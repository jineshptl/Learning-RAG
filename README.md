install UV 
$ brew install uv

sync uv to createing virtual environment 
$ uv sync


to activate virtual envirnment [creating jupyter notebook]
windows: 
$ .venv\Scripts\activate
linux or Mac
$ source .venv/bin/activate

to open the notebook
$ python -m notebook


open the 1_simple_llm_calling and create new python jupyter notebook

add your API key in .env file created on top layer of the folder

to create LLM update the line 
llm= ChatGoogleGenerativeAI(model= <"type in your ai model name">)

to call LLM 
response = llm.invoke("how many moon does Jupiter have?")
print(response.text)

Same thing for 1_simple_llm_calling & 2_health_analysis