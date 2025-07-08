# Requirements Management

This folder uses pip-tools to dynamically manage dependencies from all sub-projects.

## Setup

1. Install pip-tools:
```bash
pip install pip-tools
```

## Usage

### Generate consolidated requirements.txt
```bash
pip-compile requirements.in
```

This will:
- Read all sub-project requirements.txt files
- Resolve version conflicts
- Generate a pinned requirements.txt file

### Update all dependencies
```bash
pip-compile --upgrade requirements.in
```

### Install all requirements
```bash
pip install -r requirements.txt
```

## How it works

The `requirements.in` file uses pip-tools' `-r` flag to reference:
- `continual_learning_playground/requirements.txt`
- `evo_alg_playground/requirements.txt` 
- `rl_playground/requirements.txt`

When you run `pip-compile`, it will:
1. Read all referenced requirements files
2. Resolve dependencies and version conflicts
3. Generate a single `requirements.txt` with pinned versions
4. Include dependency trees showing where each package comes from

## Updating sub-project requirements

When you update any sub-project's requirements.txt:
1. Simply run `pip-compile requirements.in` again
2. The consolidated requirements.txt will be automatically updated

## Example workflow

```bash
# Initial setup
pip install pip-tools
pip-compile requirements.in
pip install -r requirements.txt

# After updating a sub-project's requirements
pip-compile requirements.in
pip install -r requirements.txt --upgrade
```
