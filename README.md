# Audiopedia: Audio Question Answering with Knowledge (ICASSP 2025)

This repository contains two knowledge-intensive audio question answering datasets: Single Audio Question Answering (sAQA) and Multi-Audio Question Answering (mAQA) introduced in our paper 'Audiopedia: Audio Question Answering with Knowledge' which got accepted into ICASSP 2025.

## Dataset Overview

### sAQA (Single Audio Question Answering)
- **Task**: Answer knowledge-intensive questions about named entity mentioned in a single audio clip.
- **Answer type**: Open-ended.
- **Format**: Single audio input per question.

### mAQA (Multi-Audio Question Answering)
- **Task**: Answer questions requiring reasoning over named entities across multiple audio clips.
- **Answer type**: Binary (Yes/No).
- **Format**: List of audio inputs (2) per question.

## Data Format

### sAQA Format
```json
{
    "audio_file": "sAQA/aud_files/sentence_id.wav",
    "question": "question",
    "id": "ques_id",
    "answer": "answer"
}
```

### mAQA Format
```json
{
    "audio_files": [
        "mAQA/aud_files/sentence_id_0.wav",
        "mAQA/aud_files/sentence_id_1.wav"
    ],
    "question": "question",
    "id": "ques_id",
    "answer": "answer"
}
```

## Directory Structure
```
audiopedia/
├── sAQA_release_qa.json
├── mAQA_release_qa.json
├── sAQA/
│   └── aud_files/
│       └── *.wav
└── mAQA/
    └── aud_files/
        └── *.wav

```


## Audio Files
- **sAQA audio files**: [<u>Link</u>](https://drive.google.com/file/d/1Oz_c0acc7wr7ljK6UVskSyFaPcE3ltIn/view?usp=share_link).
- **mAQA audio files**: [<u>Link</u>](https://drive.google.com/file/d/1BVl1PpuTg36GsmrAEW_nYqNAMSZJKksP/view?usp=share_link).
- **Format**: WAV
- **Generation**: Tacotron 2 text-to-speech model.


## Limitations
- Each audio sample contains only one named entity mention.
- All mentioned entities are in English.
- Less than 5% of samples may contain noise.
- Dataset is synthetic in nature.

## Citation
```
@INPROCEEDINGS{10889814,
  author={Penamakuri, Abhirama Subramanyam and Chhatre, Kiran and Jain, Akshat},
  booktitle={ICASSP 2025 - 2025 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)}, 
  title={Audiopedia: Audio QA with Knowledge}, 
  year={2025},
  volume={},
  number={},
  pages={1-5},
  keywords={Adaptation models;Benchmark testing;Signal processing;Question answering (information retrieval);Cognition;Acoustics;Speech processing;audio question answering;knowledge-intensive questions;audio entity linking},
  doi={10.1109/ICASSP49660.2025.10889814}}

```

## Contact
- Abhirama Subramanyam Penamakuri (penamakuri.1@iitj.ac.in)
- Kiran Chhatre (chhatre@kth.se)
- Akshat Jain (jain.73@iitj.ac.in)

## License
The data is released under the [MIT license](https://github.com/Abhiram4572/Audiopedia/blob/main/LICENSE).

## Acknowledgments
The knowledge base used for dataset creation is from [TextKVQA](https://textkvqa.github.io).
