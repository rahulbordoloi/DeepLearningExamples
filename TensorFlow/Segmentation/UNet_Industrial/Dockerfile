# ==============================================================================
#
# Copyright (c) 2019, NVIDIA CORPORATION. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# ==============================================================================

FROM nvcr.io/nvidia/tensorflow:20.01-tf1-py3

LABEL version="1.0" maintainer="Jonathan DEKHTIAR <jonathan.dekhtiar@nvidia.com>"

WORKDIR /opt
COPY requirements.txt /opt/requirements_unet_tf_industrial.txt

RUN python -m pip --no-cache-dir --no-cache install --upgrade pip && \
    pip --no-cache-dir --no-cache install -r /opt/requirements_unet_tf_industrial.txt

ADD . /workspace/unet_industrial
WORKDIR /workspace/unet_industrial
