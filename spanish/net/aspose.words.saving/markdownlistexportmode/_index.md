---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración MarkdownListExportMode de Aspose.Words mejora la exportación de listas a Markdown, garantizando un formato preciso y una integración perfecta para sus documentos.
type: docs
weight: 6040
url: /es/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Especifica cómo se exportan las listas a Markdown.

```csharp
public enum MarkdownListExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| MarkdownSyntax | `0` | Exportar elementos de lista compatibles con la sintaxis Markdown. |
| PlainText | `1` | Exportar elementos de la lista como texto sin formato. |

## Ejemplos

Muestra cómo se escribirán los elementos enumerados en el documento Markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilice MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax para exportar la lista.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
