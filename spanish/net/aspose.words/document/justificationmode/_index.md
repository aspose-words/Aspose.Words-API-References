---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words para .NET
description: Descubra cómo optimizar el espaciado entre caracteres de su documento con la propiedad JustificationMode. ¡Mejore la legibilidad y la presentación sin esfuerzo!
type: docs
weight: 240
url: /es/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Obtiene o establece el ajuste del espaciado de caracteres de un documento.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Ejemplos

Muestra cómo administrar el control del espaciado entre caracteres.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Ver también

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
