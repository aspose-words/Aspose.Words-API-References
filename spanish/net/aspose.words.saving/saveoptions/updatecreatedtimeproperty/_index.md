---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words para .NET
description: Optimice sus SaveOptions con la propiedad UpdateCreatedTime. Controle las actualizaciones de CreatedTime antes de guardar, lo que mejora la precisión de los datos. Valor predeterminado falso.
type: docs
weight: 160
url: /es/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Obtiene o establece un valor que determina si el[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) La propiedad se actualiza antes de guardar. El valor predeterminado es`FALSO` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Ejemplos

Muestra cómo actualizar la propiedad "CreatedTime" de un documento al guardarlo.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Esta bandera determina si la hora de creación, que es una propiedad incorporada, se actualiza.
// Si es así, entonces la fecha de la operación de guardado más reciente del documento
// con este objeto SaveOptions pasado como parámetro se utiliza como la hora de creación.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

//Abra el documento guardado y luego verifique el valor de la propiedad.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
