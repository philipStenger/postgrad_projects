# Postgraduate Projects

A collection of research and experimentation projects relating to robot learning.

## Projects

### 1. Continual Learning Playground
Experiments with continual learning algorithms and techniques including EWC, experience replay, and progressive neural networks.

### 2. Evolutionary Algorithm Playground  
Implementation and experimentation with various evolutionary algorithms including GA, DE, PSO, and multi-objective optimization.

### 3. Reinforcement Learning Playground
RL algorithms and environments including Q-Learning, DQN, REINFORCE, and OpenAI Gym integration.

## Quick Start

```bash
# Install pip-tools
pip install pip-tools
python -m venv env
env\Scripts\activate  # Windows Powershell
source env/Scripts/activate # Bash 

# Generate consolidated requirements
pip-compile requirements.in

# Install all dependencies
pip install -r requirements.txt
```

## Dependency Management

This workspace uses pip-tools to manage dependencies across all sub-projects. See [README_requirements.md](README_requirements.md) for details.

## Project Structure

```
postgrad_projects/
├── requirements.in              # Main dependency specification
├── requirements.txt            # Generated consolidated dependencies  
├── README_requirements.md      # Dependency management guide
├── continual_learning_playground/
│   ├── main.py
│   ├── requirements.txt
│   └── src/
├── evo_alg_playground/
│   ├── main.py  
│   ├── requirements.txt
│   └── src/
└── rl_playground/
    ├── main.py
    ├── requirements.txt
    └── src/
```
