---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words para .NET
description: Descubra cómo optimizar la gestión de documentos con la propiedad SplitOptions de SplitterContext para una división de contenido eficiente y flexible. Mejore su flujo de trabajo hoy mismo.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Opciones de división del documento.

```csharp
public SplitOptions SplitOptions { get; }
```

## Ejemplos

Muestra cómo dividir el documento por páginas usando el contexto.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Muestra cómo dividir el documento del flujo por páginas usando el contexto.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### Ver también

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
