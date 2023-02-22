---
title: DocSaveOptions.Password
second_title: Referencia de API de Aspose.Words para .NET
description: DocSaveOptions propiedad. Obtiene/establece una contraseña para cifrar el documento mediante el método de cifrado RC4.
type: docs
weight: 30
url: /es/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Obtiene/establece una contraseña para cifrar el documento mediante el método de cifrado RC4.

```csharp
public string Password { get; set; }
```

### Observaciones

Para guardar el documento sin encriptar, esta propiedad debe ser una cadena nula o vacía.

### Ejemplos

Muestra cómo configurar las opciones de guardado para formatos de Microsoft Word más antiguos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Establecer una contraseña que protegerá la carga del documento por Microsoft Word o Aspose.Words.
// Tenga en cuenta que esto no cifra el contenido del documento de ninguna manera.
options.Password = "MyPassword";

// Si el documento contiene una hoja de enrutamiento, podemos conservarlo mientras se guarda configurando este indicador en verdadero.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Para poder cargar el documento,
// necesitaremos aplicar la contraseña que especificamos en el objeto DocSaveOptions en un objeto LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ver también

* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../docsaveoptions/)
* asamblea [Aspose.Words](../../../)


