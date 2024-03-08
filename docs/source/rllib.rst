RLlib
=====

Parallel reinforcement learning
-------------------------------

.. note::
    Monte Carlo trajectories can be generated in parallel.

1. ``ray.put()``: send the policy to the object store so that each node can communication with it.
2. ``ray.remote()``: decorate the simulation class as Actor and generate multiple trajectories.
3. ``ray.wait()``: collect the trajectories to update the policy whenever completed.

So, it is a parameter server architecture: parameter - policy, server - environment.
