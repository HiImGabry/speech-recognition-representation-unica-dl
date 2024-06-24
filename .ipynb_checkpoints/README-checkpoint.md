# DeepSpeech

Questo progetto è stato creato per il conseguimento dell'esame di Deep Learning del seguente [corso universitario](https://unica.coursecatalogue.cineca.it/insegnamenti/2023/21411/2021/9999/11022?coorte=2022&schemaid=4601).

## Installazione ambiente
Per lo sviluppo del progetto è stato utilizzato il software [anaconda](https://www.anaconda.com/download), con la quale è possibile creare ambienti differenti. E' consigliato l'utilizzo della versione 3.10.14 di python.

Per creare un ambiente il più simile al nostro è possibile eseguire il seguente
```bash
conda create -n DL python==3.10.14
```
## Utilizzo GPU NVIDIA Tensorflow
Si consiglia di seguire la seguente [guida di tensorflow](https://www.tensorflow.org/install/pip) per l'utilizzo della propria GPU per l'addestramento dei modelli. A seconda della **scheda video utilizzata** si potrebbero riscontrare **problemi** con alcune funzioni **se si utilizza l'ambiente di miniconda insieme a WSL2**.

E' personalmente consigliato utilizzare miniconda **senza WSL2**, e installare la versione **2.10.1** di **tensorflow**.

In alternativa è possibile eseguire tutte le celle, senza problemi, utilizzando [Google Colab](https://colab.google/).

L'addestramento è stato provato su **3 GPU differenti**:
- NVIDIA L4 24GB
- NVIDIA RTX 4070ti 12GB OC
- NVIDIA A100 40GB

## Installazione pacchetti

E' consigliato l'utilizzo del gestore di pacchetti [pip](https://pip.pypa.io/en/stable/) per installare le librerie necessarie così da poter eseguire qualsiasi cella del progetto

```bash
pip install tensorflow
pip install matplotlib
pip install numpy
pip install pandas 
pip install onnxruntime
pip install tf2onnx
```

Se si utilizza la versione **2.10.1 di tensorflow** porre **massima attenzione** alla versione dei pacchetti **onnxruntime** e **tf2onnx**.

## Posizionamento dataset
Per evitare di porre modifiche al codice è consigliato posizionare i dataset utilizzati nella cartella direttamente precedente al progetto, questo perché ogni notebook elabora il dataset partendo dalla directory "../".

I dataset utilizzati sono i seguenti:
- [original_dataset](https://drive.google.com/uc?export=download&id=1_sN7ZaxH6dLv6r-mXJ91pnSez4tQu2sW)
- [reduced_dataset](https://drive.google.com/uc?export=download&id=1EwzwGoP6eYHavKA2uEJwg-60j18H6DSb)
- [noise_dataset](https://drive.google.com/uc?export=download&id=16QikfTg4wqvZPj_zyF0tPr_ELuVsK2vQ)

## Best models
Il progetto è stato strutturato in modo tale da salvare la migliore versione di ogni modello. Essendo la loro grandezza totale eccessiva, è possibile [scaricarli separatamente](https://drive.google.com/uc?export=download&id=1AJguLAGDD9I2Bh7so4wno6iMJ2sVWBmC).
E' consigliato di sostituire l'intera cartella bestmodels scaricata con quella già presente nel progetto (vuota).

## Come leggere i notebook
E' consigliata la lettura partendo dal notebook **Welcome**, e procedere secondo l'ordine da esso imposto.