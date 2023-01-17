
These are the training subsets that are used to fine-tune the hubert model and get the results in this paper: https://arxiv.org/abs/2212.01661. The [thesis](ReemGody_UTThesis.pdf) has more detailed results for the experiments and provides a deeper analysis. The appendices have the detailed statistics of the selected subsets as well as the WER for each run.

The subsets are selected from librispeech corpus and are either 10 hour or 1 hour subsets.

For each subset, we keep two files for meta-data:
1. meta.json
```json
{
    "#female speakers": 39,
    "#male speakers": 33,
    "#speakers": 72,
    "#total tokens": 95409,
    "#total unique tokens": 10517,
    "#total utts": 2996,
    "average_utt_len": 31.845460614152202,
    "max_utt_len": 80.0,
    "min_utt_len": 2.0,
    "average_utt_duration_sec": 12.028826956775703,
    "max_utt_duration_sec": 22.8,
    "min_utt_duration_sec": 1.43,
    "#books": 16,
    "#chapters": 120,
    "hours": 10.010657100694427,
    "subset": {
        "other": 1379,
        "clean": 1617
    }
}
```
2. meta_verbose.json
```json
{
    "speaker id frequency": {
        "215": 61,
        "277": 106,
        "2785": 42,
        ...
    },
    "duration_per_speaker_min": {
        "16": 13.977,
        "17": 4.309,
        "52": 3.505,
        ...
    },
    "tokens": {
        "I": 1681,
        "SEE": 125,
        "SOMEBODY": 6,
        "NOW": 189,
        "SHE": 814,
        "EXCLAIMED": 13,
       ...
    },
    "duration_per_book_min": {
        "12": 37.465,
        "16": 36.788,
        "20": 37.533,
        ...
    },
    "book distribution": {
        "12": 209,
        "16": 202,
        "20": 195,
        "33": 194,
        ...
    },
    "chapter distribution": {
        "127369": 61,
        "127368": 106,
        "163322": 42,
        "133433": 47,
        ...
    },
    "duration_per_chapter_min": {
        "348": 5.376,
        "352": 2.774,
        "354": 2.572,
        ...
    }
}
```

