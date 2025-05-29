---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words per .NET
description: Scopri il metodo GetTextShaper di ITextShaperFactory per creare uno shaper di testo personalizzato per le tue specifiche esigenze di font, migliorando la tua esperienza di rendering del testo.
type: docs
weight: 10
url: /it/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

Restituisce una nuova istanza di un text shaper per il font specificato da*fontPath* E*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontPath | String | Percorso assoluto al file del font. |
| faceIndex | Int32 | Un indice del tipo di carattere nella raccolta di caratteri TrueType, o 0 se il file di carattere specificato non è una raccolta di caratteri TrueType. |

### Guarda anche

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* spazio dei nomi [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* assemblea [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

Restituisce una nuova istanza di un text shaper per il font rappresentato da*fontBlob* E*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontId | String | Un identificatore univoco che può essere associato in modo univoco al font fornito*fontBlob* . |
| fontBlob | Byte[] | Matrice di byte con i dati del font. |
| faceIndex | Int32 | Un indice del tipo di carattere nella raccolta di caratteri TrueType, o 0 se*fontBlob* non è una raccolta di font TrueType. |

### Guarda anche

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* spazio dei nomi [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* assemblea [Aspose.Words](../../../)
