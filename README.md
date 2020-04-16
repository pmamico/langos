## Lángos

##### A Lángos egy LSTM neurális hálón alapuló magyar nyelvi modell.

|                                                | jegyzet                   | nyers adat                                                   | előkészített adat                                            | modell                                                       |
| ---------------------------------------------- | ------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Wikipédia alapú modell                         | [wiki_pretrain.ipynb](wiki_pretrain.ipynb)       | [wiki_hu.zip](https://www.dropbox.com/s/o4zv1ap6gtx7r0m/wiki.zip?dl=0) | [vocab.pkl](https://www.dropbox.com/s/jtypwtg4e2awxxm/wiki_hu_vocab.pkl?dl=0) | [wikimodell.pth](https://www.dropbox.com/s/twc1uuvfc222tej/wiki_hu.pth?dl=0) |
| port.hu dataset előállítása                    | port_hu_adatgyujtes.ipynb | [porthu.csv](https://www.dropbox.com/s/rji3oq4yrhf371k/port_hu_dataset.csv?dl=0) | [databunch.pkl](https://www.dropbox.com/s/2fkiy7agzzcgvpx/port_hu_databunch.pkl?dl=0) | -                                                            |
| port.hu komment classifier (pozitív - negatív) | port_hu_classifier.ipynb  | ↑                                                            | [encoder.pth](https://www.dropbox.com/s/khisj9kbu5qi6c9/port_hu_encoder.pth?dl=0) | [classifier.pth](https://www.dropbox.com/s/595ojtrgav68xwt/port_hu_classifier.pth?dl=0) |



### Wikipédia alapú modell

Architektúra: AWD-LSTM  
Dataset: 108k magyar wikioldal  

Vocab: 60k  
Pontosság: 26% (következő szó jóslása)  

Teljes modell:


### ULMFiT classifier (port.hu értékelések kategorizálása)

Architektúra: AWD-LSTM  
Dataseet: 45k port.hu értékelés (IMDB datasethez hasonló, pozitív-negatív)
(ebből 91% training, 9% validáció)  
Pontosság: **89%**

### Fine-tuned model (klasszikus irodalom)

Az alap nyelvi model 28%-os pontosságához képest  
klasszikus irodalmon tanított modellel a legjobb elért eredmény 55%.  
Ez inkább a dataset méretéből és tisztaságából adódik, aminek alapja 75 nyelvezetben igen hasonló könyv.  
A könyvek a BME Hunglish Corpus projektjéből származnak:  
http://mokk.bme.hu/resources/hunglishcorpus/  
UTF-8 zip: [link](https://www.dropbox.com/s/0xji1v8h414jdku/classical.zip?dl=0)  

Minden dataset és model: [dropbox](https://www.dropbox.com/sh/ynk07h7cmcygyzk/AABWMoJZHHQTprRMElAD_33ha?dl=0)
