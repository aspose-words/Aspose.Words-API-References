---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà MarkdownSaveOptions OfficeMathExportMode per personalizzare l'output di OfficeMath. Ottimizza i tuoi file con impostazioni di esportazione flessibili!
type: docs
weight: 120
url: /it/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

Specifica come OfficeMath verrà scritto nel file di output. Il valore predefinito èText .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Esempi

Mostra come OfficeMath verrà scritto nel documento.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Guarda anche

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
