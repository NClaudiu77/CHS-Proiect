# CHS-Proiect

## OCR - Recunoasterea optica a caracterelor

OCR reprezinta translatarea electronica sau mecanica a caracterelor (text fie printat, fie scris de mana)
dintr-un document scanat, dintr-o imagine in text in format electronic. OCR e un subdomeniu al cercetarii aflat la intersectia domeniilor Pattern Recognition,
AI, Computer Vision.

## Utilizari: 
> * introducerea datelor tiparite pe hartie in sisteme informatice
> * extragere de text
> * traducere automata
> * scanare carti - conversie in format electronic


## Limitari ale tehnologiei:
> * imagini neclare, distorsionate; text inclinat, rotit, incomplet;
> * existenta multiplelor fonturi
> * in cazul textului scris de mana, exista o mare variatie a modului 
	in care se poate scrie un caracter, suprapuneri de caractere, 
	ceea ce face si mai dificila problema

Pentru mai multe informatii: https://en.wikipedia.org/wiki/Optical_character_recognition

# State-Of-The-Art

## Tesseract -> https://github.com/tesseract-ocr
 Sistem OCR open-source, dezvoltat initial de HP, ca mai apoi sa fie lansat
 ca fiind open source iar din 2006 este  dezvoltat si intretinut de cei de la Google.

Avantaje :
> * a fost unul dintre primele sisteme de OCR
> * suporta multiple limbi(100 +)
> * modelele actuale folosesc tehnici de procesare a textului bazate pe algoritmi din domeniul inteligentei artificiale

Dezavantaje: 
> * funtioneaza doar pe imagini foarte clare, fara distorsiuni,  fara inclinatii ale textului, 
> *	marginile intunecate trebuie eliminate, etc.

## Keras-OCR -> https://pypi.org/project/keras-ocr/
<div align="center">
<img src = imgs/kerasocr.png alt="keras ocr" />
</div>
Sistem bazat pe doua modele :
- un model de recunoastere al textului  https://github.com/kurapan/CRNN
- un model de detectie al textului https://github.com/clovaai/CRAFT-pytorch

Avantaje: 
> * open-source,
> *  acuratete comparabila mai mare decat Tesseract
> *	 functioneaza si pe imagini cu text inclinat, putin distorsionat, etc
> *   se poate configura ( antrenand modelele de machine learning pe anumite imagini)

Dezavantaje :  
> * suporta doar limba engleza


## Cloud Vision API (Google)->  https://cloud.google.com/vision/
> * sistem proprietar, functioneaza in cloud
> * bazat pe modele preantrenate de machine learning
> * multiple functionalitati ( detectie obiecte, etichetare automata a datelor, etc)

## Multipe modele de detectie/recunoastere a textului
> * https://github.com/clovaai/CLEval
> * https://github.com/dengdan/seglink


Implementarea mea doreste sa porteze un sistem OCR pe un sistem embedded orientat pe aplicatii de AI si IOT si anume Maixduino.
Sistem bazat pe algoritmi de Deep Learning implementati cu ajutorul bibliotecilor Tensorflow,  Numpy, TensorflowLite.


