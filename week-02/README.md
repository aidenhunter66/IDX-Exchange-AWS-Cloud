# S3UploaderOnly-aiden policy explained

### Version
This is the version of the policy language. It is not today's date and not something you change. Every policy uses this exact value. 

### Statement
This is the list of rules. This policy currently has one. Bigger policies have several of them.

### Effect
This rule grants permission. The other option for this is "Deny", which blocks access and always beats an allow.

### Action
This is specifically what the user can do. In this case, you can upload (PutObject) and download (GetObject).

### Resource
Every file inside my-training-bucket-aiden and nothing else. 

### Why least privilege
This is least privilege because AWS denies everything by default. This policy opens exactly two actions on exactly one bucket's files. Everything else stays denied.

### What is a bucket?
A bucket is like a google drive or dropbox folder that lives in AWS. I make one and give it a name and put files in it. Bucket = container/folder, Object = file I sotre in it.

This policy gives access to a training bucket, allowing it to upload and download files.

The recourse ends in a /* so it points at the files in the bucket rather than the bucket itself.