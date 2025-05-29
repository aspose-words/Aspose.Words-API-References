---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words para .NET
description: ¡Proteja sus documentos con DocSaveOptions! Configure o recupere fácilmente una contraseña para el cifrado RC4 y proteja su información confidencial.
type: docs
weight: 40
url: /es/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Obtiene/establece una contraseña para cifrar el documento utilizando el método de cifrado RC4.

```csharp
public string Password { get; set; }
```

## Observaciones

Para guardar el documento sin cifrar esta propiedad debe ser`nulo` o cadena vacía.

## Ejemplos

Muestra cómo configurar las opciones de guardado para formatos más antiguos de Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Establezca una contraseña que protegerá la carga del documento por Microsoft Word o Aspose.Words.
// Tenga en cuenta que esto no encripta el contenido del documento de ninguna manera.
options.Password = "MyPassword";

// Si el documento contiene un comprobante de ruta, podemos conservarlo mientras lo guardamos estableciendo este indicador en verdadero.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

//Para poder cargar el documento,
// necesitaremos aplicar la contraseña que especificamos en el objeto DocSaveOptions en un objeto LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
