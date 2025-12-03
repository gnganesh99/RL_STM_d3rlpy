<p>This folder contains the buffer data used for training the agent.<br>
Two versions of the buffer are provided:</p>

<h3>1. <code>terminated_buffer_all.h5</code></h3>

<p>
This file contains the d3rlpy-based <code>MDPDataset</code> storing sequences of
observations, actions, rewards, and terminated flags.
</p>

<p><b>How to load the dataset:</b></p>

```python
from d3rlpy.dataset import MDPDataset
from d3rlpy.dataset import ReplayBuffer

with open(buffer_name, 'rb') as f:
    buffer = ReplayBuffer.load(f, d3rlpy.dataset.InfiniteBuffer())

buffer = load_buffer()  # if using a custom loader
episodes = buffer.episodes

for episode in episodes:
    observations = episode.observations
    actions = episode.actions
    rewards = episode.rewards
    terminated = episode.terminated





This folder contains the buffer data used for training the agent. 
Here are two versions of the buffer used to train the model.
1. "terminated_buffer_all.h5" contains the d3rlpy based MDP-dataset containing the sequence of observations, actions, rewards and terminated.
The data can be acquired using 

from d3rlpy.dataset import MDPDataset 
from d3rlpy.dataset import ReplayBuffer

 with open(buffer_name, 'rb') as f:
     buffer = ReplayBuffer.load(f, d3rlpy.dataset.InfiniteBuffer())
 buffer = load_buffer()
 episodes = buffer.episodes
 for episode in episodes:
        observations = episode.observations
        actions = episode.actions
        rewards = episode.rewards
        terminated = episode.terminated

Further documentation regaring MPDDataset can be found in the d3rlpy documantation: https://d3rlpy.readthedocs.io/en/v0.80/references/dataset.html


2. "deque_terminated_buffer_all.h5" contains the deque equivalent of the same data. 
Here is the data is indicated in the sequence: states, actions, next_states, rewards, dones.


