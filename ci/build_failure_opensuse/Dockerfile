FROM opensuse/tumbleweed
RUN zypper install -y rustup git php8-devel
WORKDIR /app
RUN rustup default stable
RUN zypper install -y php8 which clang-devel
RUN php --version
RUN git clone --depth 10 https://github.com/davidcole1340/ext-php-rs
RUN cd ext-php-rs && cargo test
