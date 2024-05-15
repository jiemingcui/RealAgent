# A quick start for training and testing

## Environment
First download Isaac Gym from the [website](https://developer.nvidia.com/isaac-gym), then follow the installation instructions.
```python
conda create -n realagent python=3.7 (or 3.7+)
conda activate realagent
pip install -r requirments.txt
```
Then git clone the code and install the package.
```python
git clone https://github.com/jiemingcui/RealAgent.git
cd YourPath/RealAgent
git clone https://github.com/leggedrobotics/rsl_rl
cd rsl_rl && pip install -e .
```
Last, adjust the path in the code to make sure the code can find the environment and the model.
```text
sys.path.append("/home/cjm/CALM_related/anyskill++/unitree_rl_gym/")
```
in ```legged_gym/scripts/train.py```, and ```legged_gym/scripts/play.py```

## Train
After environment setting and file organization, you can train the model with the following command: 
```python
python ./legged_gym/scripts/train.py --task=h1
```

## Test
After model training and saving, you can test the model with the following command: 
```python
python ./legged_gym/scripts/play.py --task=h1
```
