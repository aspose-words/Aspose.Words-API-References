---
title: SaveOptions.UpdateLastPrintedProperty
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece un valor que determina si elLastPrinted la propiedad se actualiza antes de guardar.
type: docs
weight: 170
url: /es/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Obtiene o establece un valor que determina si el[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propiedad se actualiza antes de guardar.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

### Ejemplos

Muestra cómo actualizar la propiedad "CreatedTime" de un documento al guardarlo.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// Este indicador determina si se actualiza la hora creada, que es una propiedad incorporada.
// Si es así, entonces la fecha de la operación de guardado más reciente del documento.
// con este objeto SaveOptions pasado como parámetro se utiliza como hora de creación.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Abra el documento guardado, luego verifique el valor de la propiedad.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

Muestra cómo actualizar la propiedad "Última impresión" de un documento al guardarlo.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

// Este indicador determina si se actualiza la última fecha impresa, que es una propiedad incorporada.
// Si es así, entonces la fecha de la operación de guardado más reciente del documento.
// con este objeto SaveOptions pasado como parámetro se utiliza como fecha de impresión.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// En Microsoft Word 2003, esta propiedad se puede encontrar en Archivo -> Propiedades -> Estadísticas -> Impreso.
// También se puede mostrar en el cuerpo del documento utilizando un campo PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Abra el documento guardado, luego verifique el valor de la propiedad.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


