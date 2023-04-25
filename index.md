---
marp: true
theme: default
paginate: true
header: ![height:40px](https://quantstack.net/img/logo.svg)
footer: ![height:20px](img/twitter.svg) ![height:20px](img/github.svg) @JohanMabille @jtpio @QuantStack
style: @import url('https://unpkg.com/tailwindcss@^2/dist/utilities.min.css');
---

<style>
section::after {
  content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total);
}
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>

![bg fit right:30%](https://jupyter.org/assets/homepage/main-logo.svg)

# Navigating the Jupyter Landscape

## JupyterCon 2023

---

# About

<div class="grid grid-cols-2 gap-4">
<div>

## Johan Mabille

- Technical Director at QuantStack
- Jupyter Distinguished Contributor
- Co-authored the xeus stack, the debugger in Jupyter
- Leads the development of mamba

</div>
<div>

## Jérémie Tuloup

- Technical Director at QuantStack
- Jupyter Distinguished Contributor
- Contributes to JupyterLab, Jupyter Notebook, Voilà
- Author of JupyterLite

</div>
</div>

---

![bg fit 60%](img/repos_map.svg)

---

# Jeremie slides

---

![bg fit 60%](img/client_server_kernel-0.svg)

---

# Jupyter Server

- Backend to Jupyter Web applications (not the consoles):
    - core services
    - APIs
    - REST endpoints
- Client of kernels
- Responsible for launching and keeping kernels alive
- Use the same protocol for Web apps and kernels

---

# Servers

- Jupyter Server: historical, mono user, based on tornado
- Jupyverse: alternive implementation based on async.io
- Jupyter Hub: multi-user server using Jupyter Server

---

![bg fit 60%](img/client_server_kernel-1.svg)

---

# Kernel protocol

- Documentation at https://jupyter-client.readthedocs.io/en/stable/messaging.html
- Agnostic to the language
- `jupyter_client` is the reference implementation in Python
- `xeus` is the reference implementation in C++
- implementations rely on ZeroMQ

![bg fit right:30%](https://xeus.readthedocs.io/en/latest/_images/jupyter_archi.svg)

---

![bg fit 60%](img/client_server_kernel-2.svg)

---

# Kernels

- ipykernel, reference implementation of python kernel
- kernel wrapper approach (kernels based on ipykernel)
- standalone kernels (IJulia, IRKernel)
- xeus-based kernels (xeus-cling, xeus-python, xeus-lua, etc...)

---

![bg fit 60%](img/widgets.svg)

---

# Widgets

- ipywidgets / xwidgets: basic interactive widgets (sliders, buttons, checkboxes...)
- ipyleaflet / xleaflet: interactive maps based on leaflet
- bqplot / xplot: plotting libraries implementing the grammar of graphics
- many others ....

---

Slides about Lite

---

![bg fit 60%](img/repos_map.svg)

