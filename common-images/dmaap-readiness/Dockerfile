FROM armdocker.rnd.ericsson.se/proj-ldc/common_base_os_release/sles:5.10.0-18
RUN zypper ar -C -G -f https://arm.rnd.ki.sw.ericsson.se/artifactory/proj-ldc-repo-rpm-local/common_base_os/sles/5.10.0-18 LDC-CBO-SLES \
    && zypper ref -f -r LDC-CBO-SLES \
    && zypper -n install curl \
    && zypper -n install bind-utils \
    && zypper --non-interactive in java-1.8.0 \
    && zypper clean -a \
    && zypper in -l -y --no-recommends hostname \
    && hostname
