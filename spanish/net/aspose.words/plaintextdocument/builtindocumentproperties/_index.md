---
title: PlainTextDocument.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words para .NET
description: Descubra la propiedad BuiltInDocumentProperties de PlainTextDocument para acceder y administrar fácilmente metadatos esenciales del documento para una mejor organización del mismo.
type: docs
weight: 20
url: /es/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Obtiene`BuiltInDocumentProperties` del documento.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

## Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto sin formato y luego acceder a las propiedades integradas del documento original.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.BuiltInDocumentProperties.Author = "John Doe";

doc.Save(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("John Doe", plaintext.BuiltInDocumentProperties.Author);
```

### Ver también

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
