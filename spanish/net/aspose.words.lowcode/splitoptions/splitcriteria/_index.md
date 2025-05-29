---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SplitOptions SplitCriteria mejora la gestión de documentos al dividir eficientemente su contenido en secciones manejables.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Especifica los criterios para dividir el documento en partes.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Ejemplos

Muestra cómo dividir el documento por páginas.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ver también

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
