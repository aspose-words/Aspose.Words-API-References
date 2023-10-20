---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words para .NET
description: FileFormatInfo IsEncrypted propiedad. Devolucionesverdadero si el documento está cifrado y requiere una contraseña para abrirse en C#.
type: docs
weight: 30
url: /es/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Devoluciones`verdadero` si el documento está cifrado y requiere una contraseña para abrirse.

```csharp
public bool IsEncrypted { get; }
```

## Observaciones

Esta propiedad existe para ayudarle a clasificar los documentos que están cifrados de los que no lo están. Si intenta cargar un documento cifrado usando Aspose.Words sin proporcionar una contraseña, se generará una excepción . Puede utilizar esta propiedad para detectar si un documento requiere una contraseña y realizar alguna acción antes de cargar un documento, por ejemplo, solicitar una contraseña al usuario.

## Ejemplos

Muestra cómo utilizar la clase FileFormatUtil para detectar el formato y el cifrado del documento.

```csharp
Document doc = new Document();

// Configurar un objeto SaveOptions para cifrar el documento
// con una contraseña cuando lo guardamos, y luego guardamos el documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verificar el tipo de archivo de nuestro documento, y su estado de cifrado.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
