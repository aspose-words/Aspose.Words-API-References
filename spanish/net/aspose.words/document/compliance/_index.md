---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words para .NET
description: Asegúrese de que sus documentos OOXML cumplan con los estándares de cumplimiento normativo sin esfuerzo. Nuestra herramienta analiza el contenido para verificar el cumplimiento de OOXML, mejorando así la integridad de los documentos.
type: docs
weight: 70
url: /es/net/aspose.words/document/compliance/
---
## Document.Compliance property

Obtiene la versión de conformidad con OOXML determinada a partir del contenido del documento cargado. Solo tiene sentido para documentos OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Observaciones

Si creó un nuevo documento en blanco o cargó un documento que no es OOXML, document devuelve elEcma376_2006 valor.

## Ejemplos

Muestra cómo leer la versión de conformidad con Open Office XML de un documento cargado.

```csharp
// La versión de cumplimiento varía entre documentos creados por diferentes versiones de Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Ver también

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
