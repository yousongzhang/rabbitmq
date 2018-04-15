# rabbitmq

# about blocking and non-blocking 
When one thread/process sends a message for anthor thread/process, It has two choice: wait or no wait. Synchronous messaging means is to wait until recieve response to do the next task. it called block way for it will block the thread.  Asynchronous messaging means that sender does not expect an immediate response and does not “blocks” waiting for the response. There can be a response or not, but the sender will carry out his remaining tasks.
