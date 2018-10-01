# Event Loop

How JavaScript execures asynchronous functions

call stack: a stack onto which calls are pushed when made and popped when executed

blowing the stack: infinite loop of stack placement

blocking: code that is slow, and thus blocks things from happening, like requests. not good in js cuz browsers b slow

webapi: hold onto timed tasks, shoves them into task queue when they're done. getput onto stack when stack is empty. where the nonjs code lives

set timeout for 0 will delayed something until the stack is clear

callback queue: where async tasks wait for the stack to clear before being executed when they come back from the webapi

setimetoutt not guarenteed, is a minimum. gets placed in queue when done.

rerendering has higher priority than callbacks

render queue: browser queue that gets blocked by the call stack. settimeout 0 allows rerendering to happen by making code wait

check out sprema



##prototype

All objects have a protoype, determines what manner of object they are and what functionality they have.

object.prototype = other objects sets prototype

prototype is a regular property, while [[Prototype]] indicateds inhertience

object.contstructor = prototype

can add to prototype with object.prototype.x = stuff || object.prototype = {new stuff} to overwrite

f.prototype = { constructor: f }
