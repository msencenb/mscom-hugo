---
title: "Programmatically Change S3 Storage Class To Glacier"
date: "2018-03-08"
categories: 
  - "software engineering"
tags:
  - "software engineering"
---

The glacier storage class within Amazon S3 is a great way to reduce costs for files you don't think you will ever need again, but want to have stick around just in case.

Unfortunately the AWS SDK doesn't provide a way to transition an object to the Glacier storage class; you can only transition to Infrequent Access and no further. Here is my quick hack to enable that ability:

1. Create a special folder in your S3 bucket named 'archive' (or whatever you like).
2. Create a lifecycle management rule on your S3 bucket that dictates every object within that folder (prefix 'archive') should be transitioned to Glacier storage class in 0 days.
3. Using the AWS SDK, use the 'move\_to' method to move your existing object into the archive folder when it's ready to be archived.

The downside here is that it will take until midnight to actually transition to the new storage class, and there may be extra costs incurred with the move\_to functionality (although I'm not 100% sure on this).

The upside is that to my application code, that object is in glacier storage. Given the purpose of glacier storage, that's good enough for me.
