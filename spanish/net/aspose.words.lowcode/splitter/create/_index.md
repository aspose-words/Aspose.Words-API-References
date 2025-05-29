---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words para .NET
description: Descubra cómo crear de manera eficiente una nueva instancia del procesador divisor con nuestra guía fácil de seguir para una integración perfecta y un rendimiento mejorado.
type: docs
weight: 10
url: /es/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Crea una nueva instancia del procesador divisor.

```csharp
public static Splitter Create(SplitterContext context)
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

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
