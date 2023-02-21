FROM frolvlad/alpine-glibc

RUN apk add --no-cache curl bash

EXPOSE 8080

WORKDIR /ordinals
ADD https://github.com/casey/ord/releases/download/0.5.0/ord-0.5.0-x86_64-unknown-linux-gnu.tar.gz /ordinals/ord.tar.gz
RUN tar -zxvf ord.tar.gz

RUN chmod +x /ordinals/ord
RUN ls -la
ENV RUST_LOG=debug
ENV PATH="/ordinals:$PATH"

SHELL ["/bin/bash", "-c"]

CMD ["bash"]