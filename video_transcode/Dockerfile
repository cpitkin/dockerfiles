FROM    ubuntu:latest

ENV    DEBIAN_FRONTEND noninteractive

RUN    apt-get update && \
    apt-get -y install \
      software-properties-common \
    && \
    add-apt-repository ppa:stebbins/handbrake-releases && \
    apt-get update && \
    apt-get -y install \
      ffmpeg \
      frei0r-plugins \
      handbrake-cli \
      mediainfo \
      mencoder \
      mkvtoolnix \
      mp4v2-utils \
      mplayer2 \
      ruby \
      sshfs \
    && \
    apt-get clean && \
    rm -rf /var/cache/* /var/log/apt/* /tmp/* && \
    gem install video_transcoding

CMD  transcode-video
