---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words para .NET
description: Optimice la gestión de documentos con SaveOptions UpdateLastPrintedProperty. Controle las actualizaciones de LastPrinted para un guardado eficiente y un flujo de trabajo optimizado.
type: docs
weight: 180
url: /es/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Obtiene o establece un valor que determina si el[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) La propiedad se actualiza antes de guardar.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Ejemplos

Muestra cómo actualizar la propiedad "Última impresión" de un documento al guardarlo.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Esta bandera determina si se actualiza la última fecha impresa, que es una propiedad incorporada.
// Si es así, entonces la fecha de la operación de guardado más reciente del documento
// con este objeto SaveOptions pasado como parámetro se utiliza como fecha de impresión.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// En Microsoft Word 2003, esta propiedad se puede encontrar a través de Archivo -> Propiedades -> Estadísticas -> Impreso.
// También se puede mostrar en el cuerpo del documento utilizando un campo PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

//Abra el documento guardado y luego verifique el valor de la propiedad.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
