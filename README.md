[![NPM](https://nodei.co/npm/emitter-io.png)](https://nodei.co/npm/emitter-io/)
[![NPM](https://nodei.co/npm-dl/emitter-io.png)](https://nodei.co/npm/emitter-io/)

Client library for emitter.io platform written in JavaScript for node.js.

## Installation

```
npm install emitter-io --save
```

## Example

```
// once we're connected, subscribe to the 'chat' channel
emitter.on('connect', function(){
	emitter.subscribe({
		key: "<channel key>",
		channel: "chat"
	});
});

// on every message, print it out
emitter.on('message', function(msg){
	console.log( msg.asString() );
});

// publish a message to the chat channel
emitter.publish({
	key: "<channel key>",
	channel: "chat/my_name",
	message: "hello, emitter!"
});

// actually connect to emitter service
emitter.connect();
```