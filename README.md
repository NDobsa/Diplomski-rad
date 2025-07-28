Kratki opis do sad napravljenog:
1. Fino podešavanje neuralnih jezičnih modela (koristeći Emotions Dataset)
- word2vec modela (iz gensim biblioteke) koristeći skip gram (sg) i continuous bag of words (cbow) metode
- Bert modela (iz transformers biblioteke) koristeći masked language modeling (mlm) metodu
- Kod za fino podešavanje možete pronaći u datotekama wor2vec_fine_tuning.ipynb
i bert_fine_tuning.ipynb, a gotovi fino podešeni modeli su spremljeni u mapama na google disku; 
fine_tuned_bert (https://drive.google.com/drive/folders/1WTtlzO-6Ep86G9FxrKKAlcS6s3Zj2e3k?usp=drive_link),
fine_tuned_word2vec_sg(https://drive.google.com/drive/folders/12SO4M3lOdrmVBVFlz3f7Jaj8-62AVd4X?usp=drive_link),
fine_tuned_word2vec_cbow (https://drive.google.com/drive/folders/1QxsVVTITmO3IWYf2tiVbJ7UVD5BNUb1v?usp=sharing)

2. Predikcija prisutnosti emocije u riječima (korištenjem NRC Emotion Lexicona)
- Klasifikacija algoritmom slučajnih šuma (iz sklearn biblioteke) u klase 0 (odsutnost određene emocije) i 1 (prisutnost određene emocije)
- Provedena je 5-struka unakrsna validacija i izračunate su mjere prosječne točnosti, preciznosti, odziva i F1 mjera
- Kod možete pronaći u datoteci lexicon_emotion_prediction.ipynb

- Klasifikacija dvosmjernim LSTM-om u klase 0 (odsutnost određene emocije) i 1 (prisutnost određene emocije)
- Provedena je 5-struka unakrsna validacija i izračunate su mjere prosječne točnosti, preciznosti, odziva i F1 mjera
- Kod možete pronaći u datoteci lexicon_emotion_prediction_RNN.ipynb 

3. Predikcija prisutnosti emocije u rečenicama (podaci - GoEmotions Dataset)
- Klasifikacija algoritmom slučajnih šuma (iz sklearn biblioteke) u klase 0 (odsutnost određene emocije) i 1 (prisutnost određene emocije)
- Provedena je 5-struka unakrsna validacija i izračunate su mjere prosječne točnosti, preciznosti, odziva i F1 mjera
- Kod možete pronaći u datoteci sentence_emotion_prediction.ipynb

- Klasifikacija dvosmjernim LSTM-om u klase 0 (odsutnost određene emocije) i 1 (prisutnost određene emocije)
- Provedena je 5-struka unakrsna validacija i izračunate su mjere prosječne točnosti, preciznosti, odziva i F1 mjera
- Kod možete pronaći u datoteci sentence_emotion_prediction_RNN.ipynb 

4. Predikcija prevladavajuće emocije u rečenicama (podaci - ISEAR Dataset)
- Klasifikacija algoritmom slučajnih šuma (iz sklearn biblioteke) u klase 0-6 gdje svaki razred označava određenu emociju
- Provedena je 5-struka unakrsna validacija i izračunate su mjere prosječne točnosti, preciznosti, odziva i F1 mjera
- Kod možete pronaći u datoteci sentence_strongest_emotion_prediction.ipynb

- Klasifikacija dvosmjernim LSTM-om u klase 0-6 gdje svaka klasa označava određenu emociju
- Provedena je 5-struka unakrsna validacija i izračunate su mjere prosječne točnosti, preciznosti, odziva i F1 mjera
- Kod možete pronaći u datoteci sentence_strongest_emotion_prediction_RNN.ipynb
