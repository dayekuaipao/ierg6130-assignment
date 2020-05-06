# IERG 6130 Assignment 4: Reinforcement Learning Pipeline in Practice

**Due: 11:59 pm, April 14 (Tuesday night), 2020**

**We will hold a tournament of all submitted agents. Any overdue submission will lost the opportunity to join the tournament (and the credits with that).**



## logistics

Welcome to assignment 4 of our RL course! 

In this assignment, we will implement a system of RL that allows us to train and evaluate RL agents formally and efficiently.

Different from the previous assignment, this assignment requires you to finish codes mainly in python files instead of in a jupyter notebook. This jupyter notebook is only a guideline and visualizing toolbox for you to test and play around what you have done in those python files.

In this notebook, you will go through the following components of the whole system:

* Section 1: Environment
* Section 2: Training algorithm A2C and PPO
* Section 3: Train with diverse opponents
* Section 4: Evaluate your agent and hold a tournament

Before start coding, please make sure to install the following packages:

1. pandas
2. scipy
3. seaborn
4. pygame - `pip install pygame`
5. tabulate - `pip install tabulate`
6. competitive_pong - Please install this package following guides in: https://github.com/cuhkrlcourse/competitive-pong

### Files you need to finish

The files you need to take a look and fulfill are:

1. `core/base_trainer.py` - Implement `evaluate_actions` and `compute_action`
2. `core/a2c_trainer.py` - A2C algorithm
3. `core/ppo_trainer.py` - PPO algorithm
4. `core/buffer.py` - Supporting data structure for both A2C and PPO (GAE is implemented here)
5. `core/utils/utils.py` - Implement `step_envs`
6. `train.py` - Train scripts for A2C and PPO in CartPole, Pong and competitive environment
7. `this_is_my_agent.py` - Implement `student_compute_action_function`


### Deliverable

**What you don't need to submit:**

1. **DO NOT** include notebook (the GIF is too large and useless for us) and the checkpoints of the notebook.
2. **DO NOT** include the checkpoints and logging files during the training of your agents. You only need to select the best one and submit it.

**What you need to submit:**

1. `data/evaluate_result.csv` - Your local evaluation results of your agent compared to builtin agents
2. `xxxx/checkpoint-yyyy.pkl` - **Only one** checkpoint file with `log_dir=xxxx, suffix=yyyy`, wherein yyyy is a unique name. For example, you can submit the checkpoint file: `data/0330_ppo/checkpoint-zhenghao.pkl`.
3. All other files in `assignment4/core/` and in `assignment4/` (those python files)
4. `report_SID.md` - You need to fulfill the report template `report_template.md` file with tables in `data/evaluate_result.md` and add descirption for you algorithm if necessary. Rename the file with your student ID.

Note that you should make the checkpoint file to have the correct path, and we can load your agent without errors by directly calling the function in `this_is_my_agent.py`. See `this_is_my_agent.py` and `this_is_what_we_will_do.py` for more details on the API of your agent.


### Credits

1. Tournament: 30 / 100 points - Based on your agent's performance in tournament. Rank 1 get 30 points and the last one get 10 points. Others' credits distribute uniformly in this interval. 
2. PPO: 20 / 100 points
3. A2C: 15 / 100 points
4. `BaseTrainer`, `step_envs`, `train.py`, `train_competitive.py`, `this_is_my_agent` (5) each worth 5 points.
5. Local evaluation result and description file 10 / 100 points

**Bonus**

The following cases earn you more credits (maximum 40 points)

1. Customized network structure
2. Customized opponent selecting strategies in competitive training
3. Customized algorithms
4. ...

You should clearly state your modification in the description file.

Note:

1. If your agent can not be properly loaded in TA's computer, you will lose the opportunity to participate in the tournament. 
2. We will set the working directory to `assignment4`, so that we launch tournament by directly calling `python this_is_what_we_will_do.py`.
3. Do not cheat.




## Submission Instruction


Compress the all files that **need to be submitted** in `assignment4` directory into a **zip** file, whose name follows the pattern: `"IERG6130-hw4-{name}-{id}.zip".format(name="john", id="123456")` . For instance: `IERG6130-hw4-john-123456.zip` 

Send the **zip file** and the **report file** (`report_SID.md`) to us as **two seperated files** via email: cuhkrlcourse@googlegroups.com with title in pattern `"IERG6130-hw4-{name}-{id}-2020spring".format(name="john", id="123456")` for instance: `IERG6130-hw4-john-123456-2020spring` In assignment 1, we have fully tested the googlegroups systems. It can receives all emails from students. Therefore we will not reply to you after receiving your emails.

This assignment is a bit difference since we have large checkpoint files. Please check again the excluded files.

A common checkpoint file would have size around 12Mb, so your zip file should not be greater than 20Mb.

If you find hard to include the zip file in email, please put it in OneDrive provided by CUHK and send a sharble link to us. (In that case you should still send the report file!)



## Closing Remarks


In this assignment, we implement an RL pipeline that is almost the system used in research.

This is the last assignment of this course. We appreciate you for joining this course and pay efforts to finish assignments. Hope this course can provide insights to you! 

Thanks!



------

*2019-2020 2nd term, IERG 6130: Reinforcement Learning and Beyond. Department of Information Engineering, The Chinese University of Hong Kong. Course Instructor: Professor ZHOU Bolei. Assignment author: PENG Zhenghao.*
