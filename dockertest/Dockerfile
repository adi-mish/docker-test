FROM python:3.12.0-slim

RUN useradd -ms /bin/bash admin
USER admin

# Make virtualenv
ENV VIRTUAL_ENV="/home/admin/venv"
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

# Upgrade pip
RUN pip install --no-cache-dir --upgrade pip

COPY requirements.txt /test/requirements.txt

EXPOSE 5000

WORKDIR /test
RUN pip install --no-cache-dir -r /test/requirements.txt
COPY test /test
CMD ["python", "test.py"]
