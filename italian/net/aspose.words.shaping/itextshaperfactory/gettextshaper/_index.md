---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words per .NET
description: ITextShaperFactory GetTextShaper metodo. Restituisce una nuova istanza di un modellatore di testo per il carattere specificato dafontPath EfaceIndex  in C#.
type: docs
weight: 10
url: /it/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Restituisce una nuova istanza di un modellatore di testo per il carattere specificato da*fontPath* E*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontPath | String | Un percorso assoluto al file del carattere. |
| faceIndex | Int32 | Un indice del tipo di carattere nella raccolta di caratteri TrueType, o 0 se il file di caratteri specificato non è una raccolta di caratteri TrueType. |

### Guarda anche

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* spazio dei nomi [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* assemblea [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Restituisce una nuova istanza di un modellatore di testo per il carattere rappresentato da*fontBlob* E*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontId | String | Un identificatore univoco che può essere associato in modo univoco al carattere fornito*fontBlob* . |
| fontBlob | Byte[] | Array di byte con i dati del carattere. |
| faceIndex | Int32 | Un indice del tipo di carattere nella raccolta di caratteri TrueType, o 0 se*fontBlob* non è una raccolta di caratteri TrueType. |

### Guarda anche

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* spazio dei nomi [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* assemblea [Aspose.Words](../../../)
