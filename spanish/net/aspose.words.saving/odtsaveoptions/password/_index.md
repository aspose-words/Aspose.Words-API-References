---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words para .NET
description: Proteja sus documentos con la propiedad de contraseña de OdtSaveOptions. Establezca o recupere fácilmente una contraseña para un cifrado robusto y una mayor protección de datos.
type: docs
weight: 50
url: /es/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Obtiene o establece una contraseña para cifrar el documento.

```csharp
public string Password { get; set; }
```

## Observaciones

Para guardar el documento sin cifrar esta propiedad debe ser`nulo` o cadena vacía.

## Ejemplos

Muestra cómo cifrar un documento ODT/OTT guardado con una contraseña y luego cargarlo usando Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Cree un nuevo OdtSaveOptions y pase "SaveFormat.Odt",
 // o "SaveFormat.Ott" como el formato en el que guardar el documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Si abrimos este documento con un editor apropiado,
// Nos solicitará la contraseña que especificamos en el objeto SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Si deseamos abrir o editar este documento nuevamente usando Aspose.Words,
// Tendremos que proporcionar un objeto LoadOptions con la contraseña correcta al constructor de carga.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [OdtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
