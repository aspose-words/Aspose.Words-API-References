---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words per .NET
description: Scopri come l'enum Aspose.Words XlsxSectionMode ottimizza il salvataggio dei documenti in formato XLSX, migliorando il flusso di lavoro e la gestione dei documenti.
type: docs
weight: 6530
url: /it/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Specifica come vengono gestite le sezioni quando si salva un documento nel formato XLSX.

```csharp
public enum XlsxSectionMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| MultipleWorksheets | `0` | Specifica che viene creato un foglio di lavoro separato per ogni sezione di un documento. |
| SingleWorksheet | `1` | Specifica che tutte le sezioni di un documento vengono salvate su un foglio di lavoro. |

## Esempi

Mostra come salvare un documento come foglio di lavoro separato.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Ogni sezione di un documento verrà creata come foglio di lavoro separato.
// Utilizzare 'SingleWorksheet' per visualizzare tutti i documenti su un unico foglio di lavoro.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
