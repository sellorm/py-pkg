FROM opensuse/leap:15.2

ENV OS_IDENTIFIER=opensuse-152

RUN zypper --non-interactive update

RUN zypper --non-interactive --gpg-auto-import-keys install \
    automake \
    fdupes \
    gcc \
    gcc-c++ \
    gcc-fortran \
    gdbm-devel \
    gettext-tools \
    gmp-devel \
    gzip \
    intltool \
    libbz2-devel \
    libexpat-devel \
    libffi-devel \
    libnsl-devel \
    lzma-devel \
    make \
    ncurses-devel \
    netcfg \
    openssl-devel \
    pkgconfig \
    readline-devel \
    rpm-build \
    sqlite-devel \
    tar \
    xz \
    zlib-devel \
    ruby \
    ruby-devel \
    && zypper clean

RUN gem install fpm:1.13.1 && \
    ln -s /usr/lib64/ruby/gems/2.5.0/gems/fpm-1.13.1/bin/fpm /usr/local/bin/fpm

COPY build.sh /build.sh
ENTRYPOINT [ "/build.sh" ]
CMD []
