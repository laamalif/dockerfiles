FROM debian:buster-slim
RUN apt-get update && apt-get install -y \
    curl \
 && rm -rf /var/lib/apt/lists/*
COPY gopaste /usr/bin/
VOLUME /xfs/sprunge:/sprunge
USER nobody
HEALTHCHECK --interval=30s --timeout=5s CMD curl -f http://localhost:8001 || exit 1
EXPOSE 8001
CMD ["gopaste"]
