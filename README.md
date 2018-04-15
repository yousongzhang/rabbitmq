# rabbitmq

# about blocking and non-blocking 
When one thread/process sends a message for anthor thread/process, It has two choice: wait or no wait. Synchronous messaging means that sender waits until recieves response to do the next task. it called block way for it will block the thread.  Asynchronous messaging means that sender does not expect an immediate response and does not “blocks” waiting for the response. There can be a response or not, but the sender will carry out his remaining tasks.this way called non-blocking.

RambitMQ is not-blocking way of processing message between processes/threas. sender send message through channel ,exchange, subject(routing_key).

# install rabbitmq in mac host  
brew install rabbitmq    
sudo rabbitmq-server     
install website admin page for rabbitmq:  
rabbitmq-plugins enable rabbitmq_management  

http://127.0.0.1:15672  default account guest/guest  

# python programm test rabbitmq
emit_log.py		send info(default topic) message to direct_logs    
receive_log_direct.py  recieve message from direct_logs     

# test result

Johns-Mac:rabbitmq zhangyousong$ python emit_log.py   
 [x] Sent 'info':'Hello World!'  

Johns-Mac:rabbitmq zhangyousong$ python receive_log_direct.py  info  
hello world  
 [x] 'info':'Hello World!'  
