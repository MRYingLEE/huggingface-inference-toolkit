# ARG BASE_IMAGE=nvidia/cuda:12.1.0-devel-ubuntu22.04
FROM us-docker.pkg.dev/deeplearning-platform-release/gcr.io/huggingface-pytorch-inference-cu121.2-3.transformers.4-46.ubuntu2204.py311

WORKDIR /app

#Copy model data
COPY ./model_a ./model_a

# copy entrypoint and change permissions
COPY --chmod=0755 scripts/entrypoint.sh entrypoint.sh

ENTRYPOINT ["bash", "-c", "./entrypoint.sh"]
