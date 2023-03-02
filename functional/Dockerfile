FROM rust:1.67

WORKDIR /build

RUN rustup toolchain install nightly && rustup override set nightly

RUN apt-get update && apt-get install -y ghc


# ---------------------- build compiler --------------------

COPY compiler ./compiler
RUN cargo install --path ./compiler

# ---------------------- build emulator --------------------

COPY emulator ./emulator
RUN cd emulator && ghc Emulator.hs

# ---------------------- package the built tools --------------------

WORKDIR /
RUN mkdir -p /bin && mv /build/emulator/Emulator /bin/capstone-emu
COPY scripts/capstone-run /bin/

RUN rm -rf /build

ENTRYPOINT ["capstone-run"]
