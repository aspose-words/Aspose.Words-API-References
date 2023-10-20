---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words para .NET
description: SaveOptions UpdateLastSavedTimeProperty propiedad. Obtiene o establece un valor que determina si elLastSavedTime la propiedad se actualiza antes de guardar en C#.
type: docs
weight: 180
url: /es/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Obtiene o establece un valor que determina si el[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propiedad se actualiza antes de guardar.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Ejemplos

Muestra cómo determinar si se conserva la propiedad "Última hora guardada" del documento al guardarlo.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Cuando guardamos el documento en formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
// Establece la propiedad "UpdateLastSavedTimeProperty" en "true" para
// establece la propiedad incorporada "Última hora guardada" del documento de salida en la fecha/hora actual.
// Establece la propiedad "UpdateLastSavedTimeProperty" en "false" para
// conserva el valor original de la propiedad incorporada "Última hora guardada" del documento de entrada.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.That(DateTime.Now, Is.EqualTo(lastSavedTimeNew).Within(1).Days);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
