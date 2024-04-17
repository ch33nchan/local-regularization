# local-regularization
i just tried implementing the idea behind the paper [Offline Multi-Agent Reinforcement Learning with Implicit Global-to-Local Value Regularization](https://arxiv.org/abs/2307.11620)" 

- the principle behind the implementation is OMIGA provides a principled framework to convert global-level value regularization into equivalent implicit local value regularizations and simultaneously enables in-sample learning, thus elegantly bridging multi-agent value decomposition and policy learning with offline regularizations tldr; an online multi-agent RL.

## installation
``` Bash
conda create -n env_name python=3.9
conda activate OMIGA
git clone https://github.com/ch33nchan/local-regularization.git
cd OMIGA
pip install -r requirements.txt
```

## steps to run 
prepare your datasets
```bash
([download it from here](https://cloud.tsinghua.edu.cn/d/dcf588d659214a28a777/))
then
cd omiga
python run_mujoco.py --data_dir="/data/" --scenario="Ant-v2" --agent_conf="2x4" --data_type="expert"

```

now if you want to track your progress+vitals of your performance using w&b
```bash
wandb online
export WANDB_API_KEY='YOUR W&B API KEY HERE'
python run_mujoco.py --wandb=True
```

