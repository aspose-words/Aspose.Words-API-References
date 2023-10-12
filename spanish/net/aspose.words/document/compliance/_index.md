---
title: Document.Compliance
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene la versión de cumplimiento de OOXML determinada a partir del contenido del documento cargado. Tiene sentido sólo para documentos OOXML.
type: docs
weight: 60
url: /es/net/aspose.words/document/compliance/
---
## Document.Compliance property

Obtiene la versión de cumplimiento de OOXML determinada a partir del contenido del documento cargado. Tiene sentido sólo para documentos OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

### Observaciones

Si creó un nuevo documento en blanco o cargó un documento que no sea OOXML devuelve elEcma376_2006 valor.

### Ejemplos

Muestra cómo leer la versión compatible con Open Office XML de un documento cargado.

```csharp
// La versión de cumplimiento varía entre los documentos creados con diferentes versiones de Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");

Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Ver también

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


