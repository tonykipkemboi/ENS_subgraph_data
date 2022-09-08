# **How to Query The Graph Protocol for On-Chain Data using Python**

### *A step-by-step guide on querying on-chain data from Subgraphs using Python, GraphQL, and Subgrounds.*

In this tutorial, we will query the [ENS Subgraph](https://thegraph.com/hosted-service/subgraph/ensdomains/ens) using two methods; raw [GraphQL](https://thegraph.com/docs/en/querying/graphql-api/) query and [Subgrounds](https://playgrounds-analytics.gitbook.io/playgrounds-docs/subgrounds/the-basics) library by [Playgrounds](https://www.playgrounds.network/).

The goal is for you to be able to:

- query any Subgraph data using python
- understand the two querying methods; using raw GraphQL and Subgrounds library

[What is The Graph?](./images/what_is_The_Graph.png)
## Getting Started

**Requirements:** To successfully follow this tutorial, you will need [Python 3.10](https://www.python.org/downloads/)  and [Anaconda](https://www.anaconda.com/) installed on your system.

Once you have installed Python and Anaconda, open your command line and clone this repo:

`git clone https://github.com/tonykipkemboi/ENS_subgraph_data`

Change directory into the folder:

`cd ENS_subgraph_data`

Create a python virtual environment to keep your project dependencies isolated:

`python -m venv env`

Activate the virtual environment (env); you should see the name of the environment prefixed after successful activation`(env) C:\` on Windows machine:

`.\env\Script\activate`

Now that we have our environment up and ready, let’s install some libraries that our project will depend on for querying data: 

`pip install -r requirements.txt `

To confirm you have the needed packages, use pip to check:

`python -m pip freeze`

Since we will be using the virtual environment in Jupyter Notebook, we need to add it as such;

- install [ipykernel](https://github.com/ipython/ipykernel) package which provides IPython kernel for Jupyter:

    `pip install --user ipykernel`

- add virtual environment to Jupyter by typing:

    `python -m ipykernel install --name=env`

- After running the command above, you should see something like this:

    `Installed kernelspec env in C:\ProgramData\jupyter\kernels\env`

Final step of the setup is to open Jupyter Notebook :

`jupyter notebook`

A tab will open in your browser with Jupyter on localhost. 
Locate the “New” tab and choose `env` from menu selection to open a notebook with the virtual environment we just created. 

[choose_env.png]('./images/choose_env.png')

Now we are ready to roll!