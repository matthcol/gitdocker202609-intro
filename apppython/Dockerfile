FROM python:3.13-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
	iproute2 \
	psmisc \
	tree \
	&& rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY src/ ./src/

CMD ["python", "src/main.py"]
