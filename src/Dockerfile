FROM python:3.8-slim-buster 
LABEL vendor=Rogerio\ dos\ Santos\ Silva \
    email=roger7331@gmail.com \
    version="1.0" \
    release-date="2022-04-25"
WORKDIR /app
RUN mkdir -p ./.local/bin
ENV PATH="/app/.local/bin:${PATH}"
COPY requirements.txt .
RUN pip3 install --user -r ./requirements.txt
COPY  . .
ENTRYPOINT [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]