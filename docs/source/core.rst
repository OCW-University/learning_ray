Ray Core
========


Abstractions
------------

- **driver**: the node which runs the ray code.
- **worker**: the computing nodes in the cluster.
- **object store**: a distributed memory system shared by all the nodes in the cluster.
- **task**: a function gets executed on workers instead of the driver.
- **actor**: a class hosted on workers


Six main APIs
-------------

+------------------+-------------------------------------------------------------+
| API call         | Description                                                 |
+==================+=============================================================+
| ``ray.init()``   | Initializes your Ray cluster. Pass in an address to         |
|                  | connect to an existing cluster.                             |
+------------------+-------------------------------------------------------------+
| ``ray.remote()`` | Turns functions into tasks and classes into actors.         |
+------------------+-------------------------------------------------------------+
| ``ray.put()``    | Puts values into Ray's object store.                        |
+------------------+-------------------------------------------------------------+
| ``ray.get()``    | Gets values from the object store. Returns the values you   |
|                  | put there or that were computed by a task or actor.         |
+------------------+-------------------------------------------------------------+
| ``.remote()``    | Runs actor methods or tasks on your Ray Cluster and is used |
|                  | to instantiate actors.                                      |
+------------------+-------------------------------------------------------------+
| ``ray.wait()``   | Returns two lists of object references, one with finished   |
|                  | tasks we're waiting for and one with unfinished tasks.      |
+------------------+-------------------------------------------------------------+
