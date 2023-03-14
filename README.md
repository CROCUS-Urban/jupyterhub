# Jupyterhub Configuration

Jupyterhub configuration for CROCUS.

## How to setup
We used directions from [The Littlest Jupyterhub](https://tljh.jupyter.org/en/latest/install/custom-server.html) to get started. This included the following steps

### Installing required libraries

```bash
sudo apt install python3 python3-dev git curl
```

### Run the Installer

Here, I replaced `<admin-username>` with `mgrover`

```bash
curl -L https://tljh.jupyter.org/bootstrap.py | sudo -E python3 - --admin <admin-username>
```

This was intalled on `crocus-server-04`
