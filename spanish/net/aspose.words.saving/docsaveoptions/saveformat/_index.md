---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad DocSaveOptions SaveFormat para elegir fácilmente entre los formatos Doc o Dot y guardar documentos sin problemas. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serDoc oDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
