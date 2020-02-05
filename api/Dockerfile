FROM tiangolo/uvicorn-gunicorn-fastapi:latest

COPY ./requirements.txt .
RUN pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple/
COPY ./app /app
CMD ["/start-reload.sh"]