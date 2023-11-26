FROM python:3.12.0-slim

RUN useradd -ms /bin/bash admin
USER admin

# Make virtualenv
ENV VIRTUAL_ENV="/home/admin/flaskapp/app/.venv"
RUN python3 -m venv $VIRTUAL_ENV
ENV PATH="$VIRTUAL_ENV/bin:$PATH"

COPY --chown=admin:admin app /home/admin/flaskapp/app
COPY --chown=admin:admin requirements.txt /home/admin/flaskapp/requirements.txt

RUN /bin/bash -c "pip install --no-cache-dir --upgrade pip && \
                 pip install -r /home/admin/flaskapp/requirements.txt"

EXPOSE 5000

WORKDIR /home/admin/flaskapp/app
CMD ["python3", "app.py"]



