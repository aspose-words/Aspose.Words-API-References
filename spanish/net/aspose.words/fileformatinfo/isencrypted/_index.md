---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words para .NET
description: Descubra si su documento es seguro con la propiedad FileFormatInfo IsEncrypted devuelve verdadero para archivos cifrados que necesitan una contraseña para acceder.
type: docs
weight: 40
url: /es/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Devuelve`verdadero` Si el documento está encriptado y requiere una contraseña para abrirlo.

```csharp
public bool IsEncrypted { get; }
```

## Observaciones

Esta propiedad le ayuda a distinguir entre documentos cifrados y no cifrados. Si intenta cargar un documento cifrado con Aspose.Words sin proporcionar una contraseña, se generará una excepción. Puede usar esta propiedad para detectar si un documento requiere una contraseña y tomar alguna medida antes de cargarlo, por ejemplo, solicitarla al usuario.

## Ejemplos

Muestra cómo utilizar la clase FileFormatUtil para detectar el formato y el cifrado del documento.

```csharp
Document doc = new Document();

// Configurar un objeto SaveOptions para cifrar el documento
// con una contraseña cuando lo guardamos y luego guardamos el documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

//Verificar el tipo de archivo de nuestro documento, y su estado de cifrado.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
