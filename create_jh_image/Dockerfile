FROM us.gcr.io/jupyterhub-170614/61399:v2.3

USER root
# notebook and ipykernel should already be installed. now just need jupyterhub
RUN pip install --upgrade --no-cache-dir jupyterhub

USER jovyan

WORKDIR /home/jovyan

# adding oneliner for css stuff
RUN echo "@import url(\"https://cdn.oreillystatic.com/jupyterhub/jupyterhub-theme/custom/custom.css\")" >> /opt/conda/lib/python3.6/site-packages/notebook/static/custom/custom.css

CMD jupyterhub-singleuser \
  --port=8888 \
  --ip=0.0.0.0 \
  --user="$JPY_USER" \
  --cookie-name=$JPY_COOKIE_NAME \
  --base-url=$JPY_BASE_URL \
  --hub-prefix=$JPY_HUB_PREFIX \
  --hub-api-url=$JPY_HUB_API_URL \
