# jupyterlab-google-drive

[![Build Status](https://travis-ci.org/jupyterlab/jupyterlab-google-drive.svg?branch=master)](https://travis-ci.org/jupyterlab/jupyterlab-google-drive)

Realtime collaboration and cloud storage for JupyterLab through Google Drive.

Note that this is alpha software and is rapidly changing.
Files stored on Google Drive using this plugin should still be backed-up elsewhere.

This adds a Google Drive filebrowser to the left sidepanel of JupyterLab.
When you are logged into your Google account, you will have the
files stored in it available to JupyterLab.
Notebooks and text files may be shared and edited with collaborators
in real-time, and all users will see the same changes.

For the time-being, all users running a notebook have independent kernels for
code execution, and the outputs from running cells will reflect that.

Google's servers expect traffic from computers using `http://localhost` on ports`8888` through `8899`,
and other origins will be rejected, so drive integration will not work.
See [advanced.md](advanced.md) for instructions on how to set up your own credentials with Google's servers.

## Prerequisites

* JupyterLab 0.27.0
* A Google Drive account

## Installation

To install this extension into JupyterLab (requires node 5 or later), do the following:

```bash
jupyter labextension install @jupyterlab/google-drive
```

## Development

For a development install, do the following in the repository directory:

```bash
npm install
npm run build
jupyter labextension link .
```

To rebuild the package and the JupyterLab app after making changes:

```bash
npm run build
jupyter lab build
```

## Getting Started from Scratch

- Install JupyterLab

   ```
   pip install jupyterlab
   ```

- Install the jupyterlab-google-drive extension

   ```
   jupyter labextension install @jupyterlab/google-drive
   ```

- Start JupyterLab

   ```
   jupyter lab
   ```

- Click on Google Drive tab (on left side) in JupyterLab interface and login to
  your Google Drive account.

- Have someone share a notebook or markdown file with you.

- You should now see the file in the **Shared with Me** folder in the file browser.
  Open it, and begin editing!
