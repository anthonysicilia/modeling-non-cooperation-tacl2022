# modeling-non-cooperation-tacl2022
This is the code repository for the paper "Modeling Non-Cooperative Dialogue: Theoretical and Empirical Insights" to appear in TACL.

The code to reproduce experiments is given in this repository and the data will be made available soon on OSF.

## Code
### Dependencies / Cooperative Setting
This repository is highly dependent on existing implementations for GuessWhat?! in the Cooperative Setting. Specifically, see [this repository](https://github.com/GuessWhatGame/guesswhat) provided by [Strub et al.](https://www.ijcai.org/proceedings/2017/0385.pdf) and [De Vries et al.](https://openaccess.thecvf.com/content_cvpr_2017/papers/de_Vries_GuessWhat_Visual_Object_CVPR_2017_paper.pdf). **Before running the code as described below, one should complete the steps required of this dependency** (i.e., see ```README-dependency.md``` or the original README provided by the dependency). We have already copied over required submodules and code, so these steps can be followed within our repository without making changes to the code (e.g., besides resolving small version issues). 

You can skip RL training for QGen, since our code modifies this part. We have also included some redundant data in our OSF storage, so some steps may be skipped. 

### Non-Cooperative Setting
In general, our code contributions are demarcated with ```_dim``` standing for "deception identification modification". We use ```deception``` as an identifier for components designed for the non-cooperative setting, so this can be used to help navigate the code to make modifications. 

To train the non-cooperative oracle and train QGen using RL in the non-cooperative setting, respectively, we use the following files:

* train_oracle_dim.py (replacing data with the deceptive dialogs)
* train_qgen_reinforce_2oracle_w_guesser.py

Arguments for `train_oracle_dim.py` are identical to the counterpart in the Cooperative Setting `train_oracle.py` besides the data directory. We provide some example scripts in ```oracle-examples.sh```. The script ```qgen-rl-examples.sh``` provides commands to run `train_qgen_reinforce_2oracle_w_guesser.py` as well.

### Helpful Links
Our Proposal (Non-Cooperative Setting): Forthcoming
Non-Cooperative Data: Forthcoming
Code for Cooperative Setting: https://github.com/GuessWhatGame/guesswhat
Cooperative Setting Data Proposal: https://openaccess.thecvf.com/content_cvpr_2017/papers/de_Vries_GuessWhat_Visual_Object_CVPR_2017_paper.pdf
Cooperative Setting Model Proposal: https://www.ijcai.org/proceedings/2017/0385.pdf
PyTorch Implementation of Cooperative Setting: https://github.com/shekharRavi/Beyond-Task-Success-NAACL2019

### Citation
If you use our implementation or ideas for the non-cooperative setting, please cite out paper (forthcoming).

Please also provide appropriate citation for the original cooperative setting.
