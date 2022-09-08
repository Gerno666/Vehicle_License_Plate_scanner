# Vehicle_License_Plate_scanner

Per questo progetto è stato usato l'ambiente "Jupyter Notebook" ed è stato testato con la versione Python 3.10.Per l'uso si consiglia una versione almeno pari a quella scritta sopra.

Per questo progetto sono neccesarie le seguenti librerie:

- OpenCV
- Numpy
- TensorFlow
- LabelImg
- Tesseract
- Pytesseract

Per installarle è necesario digitare da riga di comando:

- $ pip install opencv-python
- $ py -m pip install numpy
- $ pip install tensorflow
- La cartella è già stata importata ed è presente in 1_Labeling.

  Da terminale bisogna eseguire i seguenti comandi:
  
  $ pip install pyqt5 lxml
  
  $ pyrcc5 -o libs/resources.py resources.qrc
- Fare il download online di tesseract-ocr
- pip install --upgrade pytesseract

....

### Prima Parte
Nella Cartella 1_Labeling sono state scaricate varie immagini raffiguranti auto con targhe e raccolte nella cartella Images. Qua sono presenti anche file .xml, creati grazie allo strumento "LabelImg", nei quali sono racchiusi informazioni riguardo le posizioni della targhe nelle varie immagini.

È presente anche il file "01_xml_to_csv.ipynb" con il quale andremo ad estrarre queste informazioni e le salveremo nel file Excel "labels.csv".

### Seconda Parte
Nella Cartella 2_Train_Object_Detection_model andremo ad importare la cartella con le immagini e i file xml presente nella prima cartella ed anche il file "label.csv".

Con "02_Object_Detection.ipynb" andremo ad analizzare il file .csv grazie all'importazione di pandas e xml.etree.ElementTree. In seguito andremo a costruire la nostra rete neurale attraverso l'utilizzo di Tensorflow e successivamente faremo l'object detection (l'esecuzione di questa parte richiederà un pò di tempo). Alla fine salveremo il nostro modello nel file "object_detection.h5".

Con "03_Make Predictions.ipynb" invece andremo a caricare il nostro modello e faremo varie prove per testare come esso rileverà le targhe.
Una volta rilevata la targa nelle immagini, attraverso pytesseract andremo a leggere i vari caratteri presenti in essa.

### Terza Parte
Tutto ciò che abbiamo fatto finora funziona. Tuttavia c'è qualche problema, tra i quali una precisione bassa nel rilevare la targa e un elaborazione abbastanza lenta. Quindi quello che andremo a fare ora è introdurre l'utilizzo di Yolo, uno degli algoritmi di rilevamento oggetti basati su deep learning più utilizzato in circolazione.

Nel file "yolo_data_preparation" andremo a preparare i dati che ci servono. Divideremo le immagini in due cartelle, train e test e le analizzeremo di nuovo attraverso il file "labels.csv" che avevamo preparato in precedenza. Salveremo così le informazioni necessarie in dei file ".txt".

Dopo aver preparato tutto il necessario, con il file "Training_yolov5.ipynb" andremo a fare il traning dopo aver importato tutti gli strumenti necessari. Questa operazione richiederà un pò di tempo. Al termine, tutto ciò che ci servirà sarà contenuto nella cartella "yolov5/runs/train/Model2".



....

Il progetto è in corso di sviluppo.
