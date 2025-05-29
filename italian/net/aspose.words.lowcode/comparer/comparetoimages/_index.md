---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words per .NET
description: Confronta i documenti senza sforzo con CompareToImages, salvando le differenze come immagini per ogni pagina, migliorando la chiarezza e l'analisi visiva.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzato come immagine.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | String | Il documento originale. |
| v2 | String | Il documento modificato. |
| imageSaveOptions | ImageSaveOptions | Opzioni di salvataggio dell'immagine di output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzato come immagine.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | Stream | Il documento originale. |
| v2 | Stream | Il documento modificato. |
| imageSaveOptions | ImageSaveOptions | Opzioni di salvataggio dell'immagine di output. |
| author | String | Iniziali dell'autore da utilizzare per le revisioni. |
| dateTime | DateTime | Data e ora da utilizzare per le revisioni. |
| compareOptions | CompareOptions | Opzioni di confronto dei documenti. |

## Esempi

Mostra come confrontare documenti e salvare i risultati come immagini.

```csharp
// Esistono diversi modi per confrontare i documenti:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
