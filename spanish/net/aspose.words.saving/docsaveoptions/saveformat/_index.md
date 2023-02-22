---
title: DocSaveOptions.SaveFormat
second_title: Referencia de API de Aspose.Words para .NET
description: DocSaveOptions propiedad. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serDoc oDot .
type: docs
weight: 40
url: /es/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serDoc oDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../docsaveoptions/)
* asamblea [Aspose.Words](../../../)


