---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words para .NET
description: Document JustificationMode propiedad. Obtiene o establece el ajuste de espaciado entre caracteres de un documento en C#.
type: docs
weight: 230
url: /es/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Obtiene o establece el ajuste de espaciado entre caracteres de un documento.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Ejemplos

Muestra cómo gestionar el control de espaciado entre caracteres.

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
