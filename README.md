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

This was intalled on `crocus-server-05`

### Make sure the right ports are enabled

```bash
sudo tljh-config set http.port 8080
sudo tljh-config set https.port 8443
sudo tljh-config reload proxy
```

### Forward the ports on your local machine

```bash
ssh -v -N USERNAME@crocus-server-05.cels.anl.gov -L 8080:crocus-server-05.cels.anl.gov:8080
```
