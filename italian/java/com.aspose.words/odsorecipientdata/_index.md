---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words per Java"
description: "Rappresenta informazioni su un singolo record all'interno di una fonte dati esterna che deve essere escluso dall'unione di stampa in Java."
type: docs
weight: 492
url: /it/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Rappresenta informazioni su un singolo record all'interno di una fonte dati esterna che deve essere escluso dalla stampa unione.

Per saperne di più, visita l'articolo di documentazione [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Se un record deve essere unito a un documento unito, non è necessaria alcuna informazione su quel record. Tuttavia, se un determinato record non deve essere unito a un documento unito, il valore della chiave univoca per quel record deve essere memorizzato nella proprietà [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) di questo oggetto per indicare questa esclusione.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [deepClone()](#deepClone) | Restituisce una copia profonda di questo oggetto. |
| [getActive()](#getActive) | Specifica se il record dalla fonte dati deve essere importato in un documento quando viene eseguita l'unione di stampa. |
| [getColumn()](#getColumn) | Specifica la colonna nella fonte dati che contiene dati univoci per il record corrente. |
| [getHash()](#getHash) | Rappresenta il codice hash per questo record. |
| [getUniqueTag()](#getUniqueTag) | Specifica il contenuto di un determinato record nella colonna contenente dati univoci. |
| [setActive(boolean value)](#setActive-boolean) | Specifica se il record dalla fonte dati deve essere importato in un documento quando viene eseguita l'unione di stampa. |
| [setColumn(int value)](#setColumn-int) | Specifica la colonna nella fonte dati che contiene dati univoci per il record corrente. |
| [setHash(int value)](#setHash-int) | Rappresenta il codice hash per questo record. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Specifica il contenuto di un determinato record nella colonna contenente dati univoci. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Restituisce una copia profonda di questo oggetto.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Specifica se il record dalla fonte dati deve essere importato in un documento quando viene eseguita l'unione di stampa. Il valore predefinito è  true .

**Returns:**
boolean - Il valore booleano corrispondente.
### getColumn() {#getColumn}
```
public int getColumn()
```


Specifica la colonna nella fonte dati che contiene dati univoci per il record corrente. Il valore predefinito è 0.

**Returns:**
int - Il valore  int  corrispondente.
### getHash() {#getHash}
```
public int getHash()
```


Rappresenta il codice hash per questo record. Talvolta Microsoft Word utilizza [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) di un intero record invece di un valore [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). Il valore predefinito è 0.

**Returns:**
int - Il valore  int  corrispondente.
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Specifica il contenuto di un determinato record nella colonna contenente dati univoci. Il valore predefinito è  null .

**Returns:**
byte[] - Il valore byte[] corrispondente.
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Specifica se il record dalla fonte dati deve essere importato in un documento quando viene eseguita l'unione di stampa. Il valore predefinito è  true .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Specifica la colonna nella fonte dati che contiene dati univoci per il record corrente. Il valore predefinito è 0.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Rappresenta il codice hash per questo record. Talvolta Microsoft Word utilizza [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) di un intero record invece di un valore [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). Il valore predefinito è 0.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Specifica il contenuto di un determinato record nella colonna contenente dati univoci. Il valore predefinito è  null .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | byte[] | Il valore byte[] corrispondente. |

