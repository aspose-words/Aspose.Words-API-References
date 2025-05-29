---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SectionMode di XlsxSaveOptions ottimizza la gestione delle sezioni per le esportazioni XLSX, garantendo una gestione fluida dei documenti e di più fogli di lavoro.
type: docs
weight: 50
url: /it/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Ottiene o imposta il modo in cui le sezioni vengono gestite durante il salvataggio nel documento XLSX di output. Il valore predefinito èMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
