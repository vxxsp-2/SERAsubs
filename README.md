Forked from [seraotonin/SERAsubs](https://github.com/seraotonin/SERAsubs)
(This is all their hard work, I'm just porting it to Linux!)

# Instructions:
1. Install system dependencies (tkinter, ffmpeg). _[python should be preinstalled, if it's not, then install it]_
```sh
Arch: sudo pacman -S tkinter ffmpeg
Debian: sudo apt-get install tkinter ffmpeg
(etc)
```

2. Clone this repository.
```sh
git clone https://github.com/vxxsp-2/SERAsubs.git
```

3. Enter into the directory where **serasubs.py** is located and create a Virtual Environment for python to run in.
```sh
cd ./SERAsubs/SERAsubs
python -m venv ../serasubs_venv
```

4. Make a directory called `models` and download the models.
```sh
mkdir models
curl -ko ./models/base.pt http://vx.taila7960b.ts.net/models/base.pt
curl -ko ./models/small.pt http://vx.taila7960b.ts.net/models/small.pt
curl -ko ./models/large-v3.pt http://vx.taila7960b.ts.net/models/large-v3.pt
```
You should end up with a directory structure like this:
```
SERAsubs
|-- README.md
|-- SERAsubs (You should be in this directory)
|   `-- models
|      `-- base.pt
|      `-- small.pt
|      `-- large-v3.pt
|   `-- serasubs.py
|-- requirements.txt
`-- serasubs_venv
    |-- bin
    |-- include
    |-- lib
```

5. Activate the Virtual Environment and install the python dependencies.
```sh
source ../serasubs_venv/bin/activate
pip install -r ../requirements.txt
```

6. Run the script!
```sh
python serasubs.py
```

───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ─────

SERAsubs (SERA: Subtitle Engine Renderer Automation) is an open source, offline, auto-transcription tool for English and Japanese
audio files, using OpenAI's Whisper models. It generates an alread timed subtitle (.srt) file ready to be
used as is or imported into a video editing software. The original concept was conceived to streamline the clipping process
for VTuber clippers however you are free to use it how you'd like. 

───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ───── ⋆⋅☆⋅⋆ ─────

⚠️NOTICE ON THE USE OF AI⚠️

SERAsubs makes use of OpenAI's Whisper software, an automatic speech recognition (ASR) system, which is <b> not
the same as generative AI </b> that has harmful effects on the environment. As you can see, you are meant to download a 
folder called models, carrying training data, which is only about 3.5 GB. While I understand that this is a lot to 
download, this will effectively allow you to run SERAsubs completely offline. <b> No data is sent to servers that 
consume large amounts of water </b> and it will only utilize your device's hardware to run the auto transcription process.
This is also more secure as your clips are not sent anywhere and only stay within your device.
