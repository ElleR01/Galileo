
<img width="300" height="300" src="./art/galileo.png">

# Galileo Chatbot
The Chatbot of university of padova
<br>
<br>
## Setup Instructions

### file structure
the project contains two main Notebook files:
- `art folder` : contains the image of the chatbot logo
- `data folder` : the folder that contains the collected data from the website which contains four files:
  - `course_units.csv` : contains the course units data
  - `degree_courses.csv` : contains the degree courses data
  - `identity.txt` : contains information about the chatbot
  - `meta_descriptions.txt` : contains description for each column in data files
- `data-collector` : the folder that contains the code to collect the data from the university of padova website (for now it just covers Science department)
- `fine-tune` : contain the code to fine-tune the model on the collected data (llama 8b)
- `methodology-model-selection` : contains code of different model that each member tried to implement and test by using RAG and DeepEval
- `Galileo.ipynb` : the main file that contains the code of the chatbot
<br>
> Note: the data collector file is not necessary to run the chatbot, it is just to collect the data from the website and save it in a csv file
>  
> Also the collected data is already saved in the `data` folder in the project directory

<br>
<br>

### configuration
for running you need to get two API keys:
- `Groq` : to use llm's model in Inference mode (here is ```llama 8b```) [Link](https://console.groq.com/keys) .
- `Hugging Face` : to use an embedding model (here is ```all-MiniLM-L6-v2```) [Link](https://huggingface.co/settings/tokens).

To set API keys you should follow different steps for each running environment:
- **Google Colab**: you can set the API keys in secrets in left panel of the notebook.
- **Local Machine**: you can set the API keys in the `.env` file in the root of the project directory.

Use these following keys to define variables (create '.env'):
```
HUGGINGFACE_KEY=hf_...
GROQ_KEY=gsk_...
```

after setting the API keys you can run the `Galileo.ipynb` file all cells to run the chatbot.

<br>

the latest cell in the notebook will give you an interface to interact with the chatbot.
also if you run the notebook in google colab the generated link will be accessible for 72 hours for everyone to share.


## Data Collection [Optional/For Update Data]
for collecting the latest data from the university of padova website you can run the `DataCollector.ipynb` file.
it will create two csv file that contain course units and degree courses data.
then put these files in the `data` folder in the project directory.




