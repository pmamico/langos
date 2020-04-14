## Lángos

##### A Lángos egy LSTM neurális hálón alapuló magyar nyelvi model.

### Alap nyelvi model

Architektúra: AWD-LSTM  
Dataset: 108k magyar wikioldal  
Vocab: 60k  
Pontosság: 28% (következő szó jóslása)  

### Fine-tuned classifier

Architektúra: AWD-LSTM  
Dataseet: 45k port.hu értékelés (IMDB datasethez hasonló, pozitív-negatív)  
Pontosság: **90%** (kategorizálás)  

### Fine-tuned model (klasszikus irodalom)
  
Az alap nyelvi model 28%-os pontosságához képest  
klasszikus irodalmon tanított modellel a legjobb elért eredmény 55%.  
