---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words para .NET
description: MarkdownSaveOptions ListExportMode propiedad. Especifica cómo se escribirán los elementos de la lista en el archivo de salida. El valor predeterminado esMarkdownSyntax  en C#.
type: docs
weight: 60
url: /es/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Especifica cómo se escribirán los elementos de la lista en el archivo de salida. El valor predeterminado esMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Observaciones

Cuando esta propiedad se establece enPlainText todas las etiquetas de la lista se actualizan usando [`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) exportados con sus valores reales. Dichas listas pueden no ser compatibles con el formato Markdown y, en este caso, se reconocerán como texto sin formato al importarlas.

Cuando esta propiedad se establece enMarkdownSyntax, el escritor intenta export elementos de la lista de una manera que permita numerar los elementos de la lista en modo automático mediante Markdown.

## Ejemplos

Muestra cómo enumerar los elementos que se escribirán en el documento de rebajas.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Utilice MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax para exportar la lista.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Ver también

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
