# Vehicle_License_Plate_scanner

Questo progetto è stato testato con la versione Python 3.7.8.

Per l'uso si consiglia una versione almeno pari a quella scritta sopra.

Per questo progetto sono neccesarie le seguenti librerie:

- OpenCV
- Numpy
- TensorFlow
- LabelImg
- 

Per installarle è necesario digitare da riga di comando:

- $ pip install opencv-python
- $ py -m pip install numpy
- $ pip install tensorflow
- La cartella è già stata importata ed è presente in 1_Labeling.

  Da terminale bisogna eseguire i seguenti comandi:
  
  $ pip install pyqt5 lxml
  
  $ pyrcc5 -o libs/resources.py resources.qrc
- 

....

### Prima Parte
Nella Cartella 1_Labeling sono state scaricate varie immagini raffiguranti auto con targhe e raccolte nella cartella Images. Qua sono presenti anche file .xml, creati grazie allo strumento "LabelImg", nei quali sono racchiusi informazioni riguardo le posizioni della targhe nelle varie immagini.

È presente anche il file "01_xml_to_csv.ipynb" con il quale andremo ad estrarre queste informazioni e le salveremo nel file Excel "labels.csv".

....

Il progetto è in corso di sviluppo.
