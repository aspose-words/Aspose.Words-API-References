---
title: Document.JustificationMode
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene o establece el ajuste de espaciado entre caracteres de un documento.
type: docs
weight: 230
url: /es/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Obtiene o establece el ajuste de espaciado entre caracteres de un documento.

```csharp
public JustificationMode JustificationMode { get; set; }
```

### Ejemplos

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
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


