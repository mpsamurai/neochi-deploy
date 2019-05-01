FROM mpsamurai/neochi-dev-base:20190424-raspbian

COPY neochi-core/requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

COPY kinesis/requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

WORKDIR /code
COPY neochi-core/src/neochi ./neochi
COPY kinesis/src/kinesis ./kinesis

COPY run.sh .
CMD ["./run.sh"]