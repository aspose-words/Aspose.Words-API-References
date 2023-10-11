---
title: WriteProtection.ReadOnlyRecommended
second_title: Referencia de API de Aspose.Words para .NET
description: WriteProtection propiedad. Especifica si el autor del documento ha recomendado que el documento se abra como de solo lectura.
type: docs
weight: 20
url: /es/net/aspose.words.settings/writeprotection/readonlyrecommended/
---
## WriteProtection.ReadOnlyRecommended property

Especifica si el autor del documento ha recomendado que el documento se abra como de solo lectura.

```csharp
public bool ReadOnlyRecommended { get; set; }
```

### Ejemplos

Muestra cómo proteger un documento con una contraseña.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! This document is protected.");
// Ingrese una contraseña de hasta 15 caracteres de longitud y luego verifique el estado de protección del documento.
doc.WriteProtection.SetPassword("MyPassword");
doc.WriteProtection.ReadOnlyRecommended = true;

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);
Assert.IsTrue(doc.WriteProtection.ValidatePassword("MyPassword"));

// La protección no impide que el documento se edite mediante programación ni cifra el contenido.
doc.Save(ArtifactsDir + "Document.WriteProtection.docx");
doc = new Document(ArtifactsDir + "Document.WriteProtection.docx");

Assert.IsTrue(doc.WriteProtection.IsWriteProtected);

builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln("Writing text in a protected document.");

Assert.AreEqual("Hello world! This document is protected." +
                "\rWriting text in a protected document.", doc.GetText().Trim());
```

### Ver también

* class [WriteProtection](../)
* espacio de nombres [Aspose.Words.Settings](../../writeprotection/)
* asamblea [Aspose.Words](../../../)


