---
title: WriteProtection.ValidatePassword
linktitle: ValidatePassword
articleTitle: ValidatePassword
second_title: Aspose.Words para .NET
description: Proteja sus documentos con el método WriteProtection ValidatePassword. Verifique fácilmente si la contraseña coincide con la protección del documento para mayor seguridad.
type: docs
weight: 40
url: /es/net/aspose.words.settings/writeprotection/validatepassword/
---
## WriteProtection.ValidatePassword method

Devuelve`verdadero` Si la contraseña especificada es la misma que la contraseña de protección contra escritura con la que se protegió el documento. Si el documento no está protegido contra escritura con contraseña, entonces devuelve`FALSO` .

```csharp
public bool ValidatePassword(string password)
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
