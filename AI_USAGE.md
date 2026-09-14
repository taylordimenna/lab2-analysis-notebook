## AI Usage within python_notebook.ipynb
### Determining the Appropriate Analysis
I used ChatGPT (GPT-5.6) to help me determine possible ways to analysis my data based off my research question. I asked ChatGPT for examples of non-trivial transformations and analyses that would be appropriate for determining how the different asthma treatments affect gene expression. The prompt I typed into the LLM was:

    "What are some possible non-trivial transformations and analyses that would be appropriate for determining how different treatments affect gene expression."

After asking for more clarification on the dataset, it suggested many different approaches, one of which being: using a log2(FPKM + 1) transformation (to reduce the influence of high expression values) and then to use a principal component analysis (PCA) to explore the differences in the gene expressions.

I then asked for a longer explaination on that method so I could implement it within the notebook.

## AI Usage within python_notebook.html
### Converting Jupyter Notebook to HTML file
I used ChatGPT (GPT-5.6) to help convert my notebook files into a HTML version. The prompt I typed into the LLM was:

    "How do I convert a .ipybn file within VS Code to a HTML/PDF version?"

It provided me with 4 steps to follow in order to achieve this. It also told me that since I was using Jupyter in VS Code, that a HTML would be the easiest choice.

First: ChatGPT told me to install nbconvert by running:

    python -m pip install nbconvert

within PowerShell.

Second: I was told to check whether it installed correctly by running:

    python -m jupyter nbconvert --version

Since "7.17.1" was returned, it was confirmed that it was installed.

Third: I was told to confirm I was in the correct folder containing the notebook by running:

    pwd

within PowerShell.

Fourth: To create the HTML file, I was told to run:

    python -m jupyter nbconvert --to html python_notebook.ipynb

