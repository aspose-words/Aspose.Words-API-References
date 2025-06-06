---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad LoadOptions UpdateDirtyFields mejora la integridad de los datos al actualizar de forma selectiva los campos marcados como sucios para lograr un rendimiento óptimo.
type: docs
weight: 160
url: /es/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Especifica si se deben actualizar los campos con el`sucio` atributo.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## Ejemplos

Muestra cómo utilizar una propiedad especial para actualizar el resultado del campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Proporcione el valor de la propiedad "Autor" incorporada del documento y luego muéstrelo con un campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Actualizar la propiedad. El campo aún muestra el valor anterior.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Dado que el valor del campo no está actualizado, podemos marcarlo como "sucio".
// Este valor permanecerá desactualizado hasta que actualicemos el campo manualmente con el método Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Si guardamos sin llamar a un método de actualización,
    // el campo seguirá mostrando el valor desactualizado en el documento de salida.
    doc.Save(docStream, SaveFormat.Docx);

    // El objeto LoadOptions tiene una opción para actualizar todos los campos
    // marcado como "sucio" al cargar el documento.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Actualizar campos sucios como este establece automáticamente su indicador "IsDirty" en falso.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
