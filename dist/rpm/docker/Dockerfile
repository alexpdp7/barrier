FROM centos:8
RUN dnf install -y dnf-plugins-core
RUN dnf config-manager --set-enabled PowerTools
RUN dnf install -y epel-release
RUN dnf group install -y "RPM Development Tools" "Development Tools"
RUN dnf install -y libcurl-devel cmake avahi-compat-libdns_sd-devel libX11-devel libXtst-devel qt5-devel openssl-devel desktop-file-utils copr-cli
RUN mkdir -p /root/rpmbuild/SOURCES/
COPY ./src.tar.gz /root/
COPY build-in-docker /root/build-in-docker
