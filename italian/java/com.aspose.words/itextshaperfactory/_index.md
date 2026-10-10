---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words per Java"
description: "Un'interfaccia di una fabbrica per creare implementazioni di ITextShaper in Java."
type: docs
weight: 787
url: /it/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

Un'interfaccia di una fabbrica per creare implementazioni di [ITextShaper](../../com.aspose.words/itextshaper/).
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) | Restituisce una nuova istanza di un text shaper per il font rappresentato da  fontBlob  e  faceIndex . |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) | Restituisce una nuova istanza di un text shaper per il font specificato da  fontPath  e  faceIndex . |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


Restituisce una nuova istanza di un text shaper per il font rappresentato da  fontBlob  e  faceIndex .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontId | java.lang.String | Un identificatore univoco che può essere associato in modo univoco al font fornito fontBlob. |
| fontBlob | byte[] | Array di byte con i dati del carattere. |
| faceIndex | int | Un indice del carattere nella collezione di font TrueType, o 0 se  fontBlob  non è una collezione di font TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


Restituisce una nuova istanza di un text shaper per il font specificato da  fontPath  e  faceIndex .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontPath | java.lang.String | Un percorso assoluto al file del carattere. |
| faceIndex | int | Un indice del carattere nella collezione di font TrueType, o 0 se il file di carattere specificato non è una collezione di font TrueType. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
