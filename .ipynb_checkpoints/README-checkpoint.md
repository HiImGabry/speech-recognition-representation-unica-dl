# DeepSpeech

Questo progetto è stato creato per il conseguimento dell'esame di Deep Learning del seguente [corso universitario](www.google.com).

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

## Come leggere i notebook
E' consigliata la lettura partendo dal notebook **Welcome**, e procedere secondo l'ordine da esso imposto.