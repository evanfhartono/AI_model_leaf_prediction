SET UP ENVIRONTMENT
1. Install Python(https://wiki.python.org/moin/BeginnersGuide)
2. Intsall Python Package for FastAPI

   pip install -r api/requirements.txt

RUN THE PROTOTYPE
1. Run the main.py program and wait untill the server turn on
2. Run HTML file

USE THE PROTOTYPE
1. Upload Image to the dropzone
2. Tab classify button and wait for the result
3. You can use the Picture from kaggle(https://www.kaggle.com/code/gpiosenka/plants-f1-score-98-5/input)

CONFIG:
  - if the port of the configuration in main.py program doesnt match the port of the HTML live server port, turn of the server and change the port to match the HTML live server port

    origins = [
    "http://127.0.0.1:5501", 
    "http://localhost:5501",
    ]
    
    "http://127.0.0.1:[Your HTML Server Live Port]"
