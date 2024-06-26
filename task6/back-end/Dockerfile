FROM ubuntu:latest
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y python3 python3-pip python3-venv
RUN python3 -m venv /opt/venv
RUN /opt/venv/bin/pip install flask
RUN /opt/venv/bin/pip install flask-cors
WORKDIR /app
COPY api.py /app/api.py
EXPOSE 5252
CMD ["/opt/venv/bin/python3", "api.py"]