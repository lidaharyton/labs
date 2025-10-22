FROM python:3.13

# Встановлення uv
RUN pip install --no-cache-dir uv

# Встановлення Jupyter Notebook через uv
RUN pip install --no-cache-dir notebook numpy

# Робоча директорія для ноутбуків
WORKDIR /notebooks

EXPOSE 8888

# Команда запуску Jupyter
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.token=''", "--NotebookApp.password=''", "--no-browser", "--allow-root"]
