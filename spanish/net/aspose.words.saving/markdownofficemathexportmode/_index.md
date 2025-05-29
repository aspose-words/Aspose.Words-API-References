---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words para .NET
description: Descubra cómo Aspose.Words.Saving.MarkdownOfficeMathExportMode mejora la exportación de OfficeMath a Markdown, garantizando una conversión de documentos precisa y eficiente.
type: docs
weight: 6050
url: /es/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

Especifica cómo Aspose.Words exporta OfficeMath a Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | `0` | Exportar OfficeMath como texto sin formato. |
| Image | `1` | Exportar OfficeMath como imagen. |
| MathML | `2` | Exportar OfficeMath como MathML. |

## Ejemplos

Muestra cómo se escribirá OfficeMath en el documento.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
