---
title: PlainTextDocument.CustomDocumentProperties
second_title: Referencia de API de Aspose.Words para .NET
description: PlainTextDocument propiedad. ObtieneCustomDocumentProperties del documento.
type: docs
weight: 30
url: /es/net/aspose.words/plaintextdocument/customdocumentproperties/
---
## PlainTextDocument.CustomDocumentProperties property

Obtiene`CustomDocumentProperties` del documento.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

### Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto sin formato y luego acceder a las propiedades personalizadas del documento original.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.CustomDocumentProperties.Add("Location of writing", "123 Main St, London, UK");

doc.Save(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("123 Main St, London, UK", plaintext.CustomDocumentProperties["Location of writing"].Value);
```

### Ver también

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../plaintextdocument/)
* asamblea [Aspose.Words](../../../)


