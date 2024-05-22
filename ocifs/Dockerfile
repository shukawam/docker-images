FROM container-registry.oracle.com/os/oraclelinux:8

COPY ./dnf.conf /etc/dnf/dnf.conf
COPY ./ocidomain /etc/dns/vars/ocidomain
COPY ./ociregion /etc/dnf/vars/ociregion
COPY ./.oci /root/.oci/

RUN dnf update && dnf install ocifs

ENTRYPOINT [ "ocifs" ]
