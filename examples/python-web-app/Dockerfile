FROM ubuntu

WORKDIR /app

RUN apt-get update && \
    apt-get install -y python3 python3-pip

# Use --break-system-packages to install globally
RUN pip install --break-system-packages -r requirements.txt

COPY devops /app

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]





