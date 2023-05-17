## Install <a name="install"></a>

Download or clone this GitHub repo  
install requirements with:

```sh
python3 -m venv venv
. venv/bin/activate
pip3 install -r requirements.txt
```


## To start gpt4free GUI <a name="streamlit-gpt4free-gui"></a>

##### Note: streamlit app collects heavy analytics even when running locally. This includes events for every page load, form submission including metadata on queries (like length), browser and client information including host ips. These are all transmitted to a 3rd party analytics group, Segment.com.

Move `streamlit_app.py` from `./gui` to the base folder then run:  
`streamlit run streamlit_app.py` or `python3 -m streamlit run streamlit_app.py`

```sh
cp gui/streamlit_app.py .
streamlit run streamlit_app.py
```


## Docker <a name="docker-instructions"></a>

Build

```
docker build -t gpt4free:latest .
```

Run

```
docker run -p 8501:8501 gpt4free:latest
```

## Deploy using docker-compose

Run the following:

```
docker-compose up --build -d
```
