# lsm_prensa_curated
The lsm_prensa_curated is a manually curated annotation resource for continuous
gloss-free Mexican Sign Language (Lengua de Señas Mexicana, LSM) translation 
 into Spanish. This repository contains a JSON file describing 1,000 video–text 
 samples derived from 55 Mexican presidential morning press conference 
 broadcasts with simultaneous LSM interpretation. The annotations support 
 gloss-free sign language translation without intermediate gloss labels.

Each sample includes a Spanish transcription manually reviewed and corrected 
against the content signed by the interpreter. The original automatic speech 
recognition (ASR) caption is also retained, enabling comparisons between 
automatically generated captions and manually curated transcriptions.


## Record format

Each line is one JSON object describing one video--text sample.

```json
{
    "id": "lsm_prensa_20241002_L08_00001",
    "raw_video_id": "lsm_prensa_20241002",
    "text": "muy buenos días a todos a todas, hoy",
    "asr_text": "Muy buenos días a todos a todas el día de hoy primera mañanera del pueblo",
    "delta_margin": 0.5,
    "sample": {
        "t_start": 0.0,
        "t_end": 9.6,
        "video_path": "samples/videos/lsm_prensa_20241002/lsm_prensa_20241002_L08_00001.mp4"
    },
    "raw": {
        "t_start": 613.58,
        "t_end": 623.18,
        "video_path": "interpreter_videos/videos/lsm_prensa_20241002.mp4"
    },
    "num_frames": 240,
    "url": "https://www.youtube.com/watch?v=EGG3yRO7fAo",
    "split": "train"
}
```

The curated dataset comprises 920 training samples, 40 validation samples, and 
40 test samples.

This deposit contains annotations and metadata only; video files are not 
included. The YouTube URLs identify the original broadcasts, while the relative
video paths describe the file organization used during preprocessing. These 
paths are not download links.

The resource was developed for the study “Two Streams, One Sign: SignOmni, a 
Multimodal Architecture for Gloss-Free Sign Language Translation.” It supports 
research on continuous LSM translation, video–text learning, and transcription 
quality. Users should consider its limited size, its focus on presidential 
press conferences, and possible temporal mismatches between signing and 
segment boundaries. Access to the source footage depends on the continued 
availability of the original broadcasts.