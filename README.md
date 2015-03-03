# JazminServer
JazminServer is a Java based application/message/rpc server.
# Main features
* Core
  * Log 
  * AopDispatcher
  * JobScheduler
  * ApplicationLoader
  * BootLoader
  * JobScheduler
  * TaskScheduler
* Drivers
  * HttpDriver
  * JDBCDriver
  * LuceneDriver
  * MemcachedDriver
  * RPCDriver
* RPCServer
  * Server push message to client
  * Client proxy 
* MessageServer
  * Session management
  * Asyc service
  * Continuation service
  * Oneway service
  * amf/json/zjson message format
* WebServer
  * Jetty based webserver
  * Simple MVC framework
* ConsoleServer
  * SSH based monitor server
  * Piped command
  * REPL env
  
# Demo
Start a rpc server and register remote server
<pre>
   Jazmin.addServer(new ConsoleServer());
   RPCServer rpcServer=new RPCServer();
   rpcServer.registerService(new TestRemoteServiceImpl());
   Jazmin.addServer(rpcServer);
   Jazmin.start();
</pre>
