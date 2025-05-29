---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.Saving.MarkdownOfficeMathExportMode migliora l'esportazione di OfficeMath in Markdown, garantendo una conversione dei documenti accurata ed efficiente.
type: docs
weight: 6050
url: /it/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Specifica come Aspose.Words esporta OfficeMath in Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Text | `0` | Esporta OfficeMath come testo normale. |
| Image | `1` | Esporta OfficeMath come immagine. |
| MathML | `2` | Esporta OfficeMath come MathML. |

## Esempi

Mostra come OfficeMath verrà scritto nel documento.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
