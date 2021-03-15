# Swedish Kaldi Profile

A [Rhasspy](https://github.com/rhasspy/rhasspy) profile for Swedish (`sv`).

Includes:

* A [Kaldi nnet3](https://kaldi-asr.org/doc/dnn3.html) speech to text model
    * See files in `acoustic_model/`
    * Recipe created with [ipa2kaldi](https://github.com/rhasspy/ipa2kaldi)
    * Word error rate: 4.84%
    * Trained on:
        * [NST Swedish ASR Database](https://www.nb.no/sprakbanken/en/resource-catalogue/oai-nb-no-sbr-56/) (378 hours)
        * [Common Voice](https://commonvoice.mozilla.org) (15 hours)
* An [IPA](https://en.wikipedia.org/wiki/International_Phonetic_Alphabet) pronunciation lexicon
    * See `base_dictionary.txt.gz`
* A [phonetisaurus](https://github.com/AdolfVonKleist/Phonetisaurus) grapheme to phoneme model for predicting word pronunciations
    * See `g2p.fst.gz`
    * Trained on `base_dictionary.txt.gz`
* A tri-gram [ARPA language model](https://cmusphinx.github.io/wiki/arpaformat/)
    * See `base_language_model.txt.gz`
    * Text from audio transcriptions, [Common Voice](https://github.com/mozilla/common-voice/tree/master/server/data/sv-SE), [Universal Dependencies](https://universaldependencies.org/), and [Oscar](https://oscar-corpus.com/)
