# Dockerfile for PyStan and PyMC3

Note: **Use only in your local machine!**

- [Dockerfile](./Dockerfile)
  - PyStan
  - PyMC3
  - JupyterLab
- Build in this directory: `docker build -t stan-mc3:2 .`
- Run: `docker run --rm --name stan-mc3 -d -p 8888:8888 -v ~/workdir:/workdir stan-mc3:2`
  - `/workdir` is the default working directory.
  - JupyterLabs use port `8888`.
- Access to JupyterLab: http://localhost:8888/
