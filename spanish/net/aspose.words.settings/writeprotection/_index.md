---
title: WriteProtection Class
linktitle: WriteProtection
articleTitle: WriteProtection
second_title: Aspose.Words para .NET
description: Aspose.Words.Settings.WriteProtection clase. Especifica la configuración de protección contra escritura para un documento en C#.
type: docs
weight: 5970
url: /es/net/aspose.words.settings/writeprotection/
---
## WriteProtection class

Especifica la configuración de protección contra escritura para un documento.

Para obtener más información, visite el[Proteger o cifrar un documento](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) artículo de documentación.

```csharp
public class WriteProtection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [IsWriteProtected](../../aspose.words.settings/writeprotection/iswriteprotected/) { get; } | Devoluciones`verdadero` cuando se establece una contraseña de protección contra escritura. |
| [ReadOnlyRecommended](../../aspose.words.settings/writeprotection/readonlyrecommended/) { get; set; } | Especifica si el autor del documento ha recomendado que el documento se abra como de solo lectura. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetPassword](../../aspose.words.settings/writeprotection/setpassword/)(*string*) | Establece la contraseña de protección contra escritura para el documento. |
| [ValidatePassword](../../aspose.words.settings/writeprotection/validatepassword/)(*string*) | Devoluciones`verdadero` si la contraseña especificada es la misma que la contraseña de protección contra escritura con la que se protegió el documento. Si el documento no está protegido contra escritura con contraseña, entonces regresa`FALSO` . |

## Observaciones

La protección contra escritura especifica si el autor ha recomendado que el documento se abra como de solo lectura y/o requiera una contraseña para modificar un documento.

La protección contra escritura es diferente de la protección de documentos. La protección contra escritura se especifica en Microsoft Word en las opciones del cuadro de diálogo Guardar como.

No crea instancias de esta clase directamente. Puede acceder a la configuración de protección de documentos a través del[`WriteProtection`](../../aspose.words/document/writeprotection/) propiedad.

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

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
