#RUN THESE COMMANDS IF U ARE UNABLE TO CREATE SECOND KIND CLUSTER IT WILL INCRESES THE LIMIT 
sudo sysctl fs.inotify.max_user_watches=524288
What it does: Sets the maximum number of file or directory watches available to a real user ID to 524288.
- A watch monitors a file or directory for events such as modifications, creation, or deletion.
- Applications can use these events to detect changes without repeatedly scanning the file system.
- Increasing the limit can help applications that monitor many files avoid errors caused by exhausting available watches.

sudo sysctl fs.inotify.max_user_instances=512
What it does: Sets the maximum number of inotify instances a real user ID can create to 512.
- An instance is an inotify monitoring interface created by an application.
- Each instance can contain multiple watches.
- Increasing this limit allows applications to create more independent inotify monitoring instances.
