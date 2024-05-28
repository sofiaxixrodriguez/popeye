#FROM python:latest
#
#WORKDIR /app
#
#ADD . /app
#
#RUN pip3 install --no-cache-dir -r requirements.txt
#
#EXPOSE 80
#
#CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]
#


##FROM python:3
##
##WORKDIR /usr/src/app
##
##COPY requirements.txt ./
##RUN pip install --no-cache-dir -r requirements.txt
##
##EXPOSE 80
##
##COPY . .
##
##CMD [ "python", "./app.py" ]



FROM python:3-slim
WORKDIR /app
ADD requirements.txt /app/requirements.txt
RUN pip3 install -r requirements.txt
ADD . /app
EXPOSE 80

CMD flask run --host=0.0.0.0 --port=80