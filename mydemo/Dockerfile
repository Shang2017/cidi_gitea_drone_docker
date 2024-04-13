FROM mingc/android-build-box:latest

ARG flutter_version

ENV FLUTTER_HOME=${HOME}/sdks/flutter \
    FLUTTER_ROOT=$FLUTTER_HOME \
    FLUTTER_VERSION=$flutter_version \
    PUB_HOSTED_URL=https://pub.flutter-io.cn \
    FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn

RUN mkdir -p ${FLUTTER_HOME}

ENV PATH ${PATH}:${FLUTTER_HOME}/bin:${FLUTTER_HOME}/bin/cache/dart-sdk/bin

RUN git clone --branch ${FLUTTER_VERSION} https://github.com/flutter/flutter.git ${FLUTTER_HOME} && \
       flutter doctor

