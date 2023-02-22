---
title: Field.IsDirty
second_title: Referencia de API de Aspose.Words para .NET
description: Field propiedad. Obtiene o establece si el resultado actual del campo ya no es correcto obsoleto debido a otras modificaciones realizadas en el documento.
type: docs
weight: 40
url: /es/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento.

```csharp
public bool IsDirty { get; set; }
```

### Ejemplos

Muestra cómo usar una propiedad especial para actualizar el resultado del campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Proporcione el valor de propiedad "Autor" integrado del documento y luego muéstrelo con un campo.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Actualizar la propiedad. El campo aún muestra el valor anterior.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Dado que el valor del campo está desactualizado, podemos marcarlo como "sucio".
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

    // La actualización de campos sucios como este establece automáticamente su indicador "IsDirty" en falso.
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

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)


