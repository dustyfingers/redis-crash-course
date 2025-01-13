basic redis commands

<!-- add a key -->

SET name 'kyle'
SET age 26

<!-- get a key -->

GET age

<!-- delete a key -->

DEL age

<!-- check if key exists -->

EXISTS number
EXISTS name

<!-- get all keys - KEYS * -->

KEYS \*

<!-- flush cache -->

flushall

<!-- make key expire -->
<!-- expires name key in 10s -->

expire name 10

<!-- set a key with an expiration date -->

setex name 10 kyle

<!-- lists -->

<!-- push item to list -->

lpush friends john

get friends // doesnt work

lrange friends 0 -1 // see all items in list

lpush friends sally // add to beginning of list

lrange friends 0 -1

rpush friends mike // add to end of list

lrange friends 0 -1

lpop friends // remove from beginning of array
rpop friends // remove from end of array

<!-- sets - unique array -->

sadd hobbies "jiu-jitsu" // add item to set
smembers hobbies // grab all members of set
srem hobbies "jiu jitsu" // remove item from set

<!-- hash - kv pair, doesnt allow nesting -->

hset person name kyle // set kv pair on hash 'person'
hget person name // returns kyle
hgetall person // gets all fields of person
hexists person name // returns 1
hexists person age // returns 0
