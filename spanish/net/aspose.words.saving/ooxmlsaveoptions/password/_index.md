---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words para .NET
description: ¡Proteja sus documentos con OoxmlSaveOptions! Configure fácilmente una contraseña para el cifrado utilizando el estándar ECMA376 para una mayor protección de datos.
type: docs
weight: 60
url: /es/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Obtiene/establece una contraseña para cifrar el documento utilizando el algoritmo de cifrado estándar ECMA376.

```csharp
public string Password { get; set; }
```

## Observaciones

Para guardar el documento sin cifrar esta propiedad debe ser`nulo` o cadena vacía.

## Ejemplos

Muestra cómo crear un documento Office Open XML cifrado con contraseña.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

//No podremos abrir este documento con Microsoft Word o
// Aspose.Words sin proporcionar la contraseña correcta.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Abra el documento cifrado pasando la contraseña correcta en un objeto LoadOptions.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
