---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words para .NET
description: Optimice sus opciones de guardado con la propiedad UpdateLastSavedTime. Controle las actualizaciones de LastSavedTime para una gestión eficiente de los datos y un mejor rendimiento.
type: docs
weight: 190
url: /es/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Obtiene o establece un valor que determina si el[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) La propiedad se actualiza antes de guardar.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Ejemplos

Muestra cómo determinar si se debe conservar la propiedad "Última hora de guardado" del documento al guardarlo.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Cuando guardamos el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardar del documento para modificar la forma en que guardamos el documento.
// Establezca la propiedad "UpdateLastSavedTimeProperty" en "verdadero" para
// Establezca la propiedad incorporada "Última hora de guardado" del documento de salida en la fecha y hora actuales.
// Establezca la propiedad "UpdateLastSavedTimeProperty" en "falso" para
// conserva el valor original de la propiedad incorporada "Última hora de guardado" del documento de entrada.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
