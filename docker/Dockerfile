FROM matlabruntime/r2023a/release/update5/300000000000000000

# Create the directory
RUN mkdir -p /usr/bin/mlrtapp

COPY /build/mat2json /usr/bin/mlrtapp
COPY /build/run_mat2json.sh /usr/bin/mlrtapp
COPY /build/readme.txt /usr/bin/mlrtapp

RUN chmod -R a+rX /usr/bin/mlrtapp/

# Set the MCR_CACHE_ROOT environment variable
ENV MCR_CACHE_ROOT=/tmp

# Add MATLAB app directory to PATH
ENV PATH="/usr/bin/mlrtapp:${PATH}"