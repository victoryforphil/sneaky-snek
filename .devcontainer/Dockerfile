# Use the official Python image
FROM python:3.10-slim

# Set the working directory in the container
WORKDIR /workspace

# Copy requirements and install them
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Expose port for Jupyter Notebook
EXPOSE 8888

# Copy the entire project into the container
COPY . /workspace

# Set the default command to run Jupyter Notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--no-browser", "--allow-root", "--notebook-dir=/workspace/notebooks", "--NotebookApp.token=''", "--NotebookApp.password=''"] 