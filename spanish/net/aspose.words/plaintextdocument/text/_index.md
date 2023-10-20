---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: PlainTextDocument Text propiedad. Obtiene el contenido textual del documento concatenado como una cadena en C#.
type: docs
weight: 40
url: /es/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Obtiene el contenido textual del documento concatenado como una cadena.

```csharp
public string Text { get; }
```

## Ejemplos

Muestra cómo cargar el contenido de un documento de Microsoft Word en texto sin formato.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ver también

* class [PlainTextDocument](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
