---
title: WriteProtection.IsWriteProtected
linktitle: IsWriteProtected
articleTitle: IsWriteProtected
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsWriteProtected de WriteProtection, verifique fácilmente si una contraseña de protección contra escritura está activa para mejorar la seguridad y la integridad de los datos.
type: docs
weight: 10
url: /es/net/aspose.words.settings/writeprotection/iswriteprotected/
---
## WriteProtection.IsWriteProtected property

Devuelve`verdadero` cuando se establece una contraseña de protección contra escritura.

```csharp
public bool IsWriteProtected { get; }
```

## Ejemplos

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

//La protección no impide que el documento se edite mediante programación ni cifra el contenido.
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
* espacio de nombres [Aspose.Words.Settings](../../../aspose.words.settings/)
* asamblea [Aspose.Words](../../../)
