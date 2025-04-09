FROM python:3.12

# Install system dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    gcc \
    libc6-dev \
    libonig-dev \  
    && rm -rf /var/lib/apt/lists/*

# Install Python dependencies
RUN pip install --no-cache-dir \
    ansible \
    ansible-navigator \
    ansible-builder \
    psycopg2-binary

WORKDIR /ansible

ENTRYPOINT ["/bin/sh"]