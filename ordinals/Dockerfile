FROM frolvlad/alpine-glibc

RUN apk add --no-cache curl bash

SHELL ["/bin/bash", "-c"]

EXPOSE 8080

WORKDIR /ordinals
ADD https://github.com/casey/ord/releases/download/0.5.1/ord-0.5.1-x86_64-unknown-linux-gnu.tar.gz /ordinals/ord.tar.gz
RUN tar -zxvf ord.tar.gz

RUN chmod +x /ordinals/ord
RUN ls -la
ENV RUST_LOG=debug
# ENV PATH="/ordinals:$PATH"

ADD https://bitcoincore.org/bin/bitcoin-core-24.0.1/bitcoin-24.0.1-x86_64-linux-gnu.tar.gz /bitcoin/bitcoin.tar.gz
RUN tar -zxvf /bitcoin/bitcoin.tar.gz
RUN mv bitcoin-24.0.1/bin/bitcoin-cli /usr/local/bin

CMD ["init.sh"]