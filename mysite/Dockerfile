# FROM python:3.7

# # Allows docker to cache installed dependencies between builds
# # COPY requirements.txt requirements.txt
# # RUN pip install --no-cache-dir -r requirements.txt

# # Mounts the application code to the image
# COPY . code
# WORKDIR /code
# COPY requirements.txt .
# RUN pip install -r requirements.txt

# EXPOSE 8000

FROM python:3
ENV PYTHONBUFFER=1
WORKDIR /code
COPY requirements.txt .
RUN pip install -r requirements.txt
EXPOSE 8000

# runs the production server
ENTRYPOINT ["python", "mysite/manage.py"]
CMD ["runserver", "0.0.0.0:8000"]