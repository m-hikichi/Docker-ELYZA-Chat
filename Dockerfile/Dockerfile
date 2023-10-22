FROM nvidia/cuda:12.2.2-cudnn8-runtime-ubuntu20.04

RUN ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime
RUN apt update && apt -y upgrade
RUN apt install -y python3-pip

COPY requirements.txt .
RUN pip install -r requirements.txt

# install model
RUN mkdir -p /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/resolve/main/pytorch_model-00001-of-00002.bin
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/resolve/main/pytorch_model-00002-of-00002.bin
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/raw/main/config.json
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/raw/main/pytorch_model.bin.index.json
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/raw/main/special_tokens_map.json
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/raw/main/tokenizer.json
RUN wget -P /root/.cache/huggingface/hub/models--elyza--ELYZA-japanese-Llama-2-7b-fast-instruct/snapshots/89de33d1ad568855853196802aeaecd799c6586f/ https://huggingface.co/elyza/ELYZA-japanese-Llama-2-7b-fast-instruct/raw/main/tokenizer_config.json
