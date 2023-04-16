## Requirements

### Python venv

#### Install Python

Note, the version needs to be 3.6.8
```
choco install python3 --version 3.6.8
```

#### Setup venv

```
python -m venv .venv
```

After create env, activate it
```
.venv/Scripts/Activate.ps1
```

Upgrade `pip`

```
python -m pip install --upgrade pip
```

And install all dependencies

```
pip install -r requirements.txt
```