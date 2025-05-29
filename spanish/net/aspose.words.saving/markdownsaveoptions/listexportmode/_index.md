---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad ListExportMode de MarkdownSaveOptions, que controla cómo se muestran los elementos de la lista. ¡Optimice sus archivos con la flexible sintaxis de Markdown!
type: docs
weight: 110
url: /es/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

Especifica cómo se escribirán los elementos de la lista en el archivo de salida. El valor predeterminado esMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## Observaciones

Cuando esta propiedad se establece enPlainText Todas las etiquetas de lista se actualizan mediante[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) y se exportan con sus valores reales. Estas listas pueden no ser compatibles con el formato Markdown y, en este caso, se reconocerán como texto sin formato al importarlas.

Cuando esta propiedad se establece enMarkdownSyntax, el escritor intenta exportar elementos de lista de manera tal que permita numerar los elementos de lista en modo automático mediante Markdown.

## Ejemplos

Muestra cómo se escribirán los elementos enumerados en el documento Markdown.

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
