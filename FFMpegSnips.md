# USefull Snippets for FFMPEG

### Combine two InputStreams where one is louder
---
ffmpeg -y -i A.mp3 -i B.mp3 -filter_complex "[0:0]volume=0.2[a];[1:0]volume=0.5[b];[a][b]amix=inputs=2:duration=longest" -c:a libmp3lame output1.mp3
---
### Find all webm files in current folder and convert to MP3
find . -type f -iname "*.webm" -exec bash -c 'FILE="$1"; ffmpeg -i "${FILE}" -vn -ab 128k -ar 44100 -y "${FILE%.webm}.mp3";' _ '{}' \;
---
