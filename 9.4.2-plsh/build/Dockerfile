FROM postgres:9.4.2

MAINTAINER tsaikd <tsaikd@gmail.com>

RUN apt-get update
RUN apt-get install -qy git make "postgresql-server-dev-${PG_MAJOR}"
RUN git clone https://github.com/petere/plsh /tmp/plsh
WORKDIR /tmp/plsh
RUN make
RUN make install
RUN tar czpf /postgres-${PG_MAJOR}-plsh.tar.gz /usr/lib/postgresql/${PG_MAJOR}/lib/plsh.so /usr/share/postgresql/${PG_MAJOR}/extension/plsh*
ADD docker_cmd_install.sh /install.sh

