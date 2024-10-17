FROM ubuntu:20.04

RUN apt-get update -y && \
    apt-get install -y --no-install-recommends python3-pip python-dev build-essential && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
    
COPY ./service /App

WORKDIR /App

RUN pip3 install --upgrade pip && \
    pip3 install -r ./requirements.txt
    
EXPOSE 80

ENTRYPOINT ["python3"]

CMD ["mythicalMysfitsService.py"]
