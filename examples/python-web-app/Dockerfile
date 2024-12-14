FROM ubuntu

WORKDIR /app

# Install pipx
RUN apt-get update && \
    apt-get install -y python3 python3-pip python3-venv && \
    pip install --user pipx && \
    python3 -m pipx ensurepath

COPY requirements.txt /app
COPY devops /app

# Install requirements using pipx
RUN pipx install -r requirements.txt

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
