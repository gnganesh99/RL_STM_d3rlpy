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
```


<p> Further documentation regarding <code>MDPDataset</code> can be found in the d3rlpy documentation:<br> <a href="https://d3rlpy.readthedocs.io/en/v0.80/references/dataset.html"> https://d3rlpy.readthedocs.io/en/v0.80/references/dataset.html </a> </p> 




<h3>2. <code>deque_terminated_buffer_all.h5</code></h3> <p> This file contains the deque-equivalent of the same data.<br> The data are stored in the sequence: </p> <pre> states, actions, next_states, rewards, dones </pre>




Further documentation regaring MPDDataset can be found in the d3rlpy documantation: https://d3rlpy.readthedocs.io/en/v0.80/references/dataset.html




