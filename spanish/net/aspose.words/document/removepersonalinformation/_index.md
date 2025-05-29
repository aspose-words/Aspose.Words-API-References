---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words para .NET
description: Garantice la privacidad con la función Eliminar información personal de documentos en Word, que elimina automáticamente los datos del usuario de los comentarios y propiedades al guardar.
type: docs
weight: 360
url: /es/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Obtiene o establece un indicador que indica que Microsoft Word eliminará toda la información del usuario de los comentarios, revisiones y propiedades del documento al guardar el documento.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Ejemplos

Muestra cómo habilitar la eliminación de información personal durante un guardado manual.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar algún contenido con información personal.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Esta bandera es equivalente a Archivo -> Opciones -> Centro de confianza -> Configuración del centro de confianza... ->
// Opciones de privacidad -> "Eliminar información personal de las propiedades del archivo al guardar" en Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Esta opción no tendrá efecto durante una operación de guardado realizada con Aspose.Words.
//Los datos personales se eliminarán de nuestro documento con la bandera activada cuando lo guardemos manualmente usando Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
