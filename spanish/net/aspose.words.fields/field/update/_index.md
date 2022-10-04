---
title: Update
second_title: Referencia de API de Aspose.Words para .NET
description: Realiza la actualización del campo. Se lanza si el campo ya se está actualizando.
type: docs
weight: 140
url: /es/net/aspose.words.fields/field/update/
---
## Update() {#update}

Realiza la actualización del campo. Se lanza si el campo ya se está actualizando.

```csharp
public void Update()
```

### Ejemplos

Muestra cómo insertar un campo en un documento usando FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte dos campos mientras pasa una bandera que determina si actualizarlos a medida que el constructor los inserta.
// En algunos casos, la actualización de campos puede ser computacionalmente costosa y puede ser una buena idea posponer la actualización.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Tendremos que actualizar estos campos usando los métodos de actualización manualmente.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

Muestra cómo dar formato a los resultados de los campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use un generador de documentos para insertar un campo que muestre un resultado sin formato aplicado.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// Podemos aplicar un formato al resultado de un campo usando las propiedades del campo.
// A continuación se muestran tres tipos de formatos que podemos aplicar al resultado de un campo.
// 1 - Formato numérico:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - Formato de fecha/hora:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - Formato general:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// Podemos eliminar nuestros formatos para revertir el resultado del campo a su forma original.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)

---

## Update(bool) {#update_1}

Realiza una actualización de campo. Se lanza si el campo ya se está actualizando.

```csharp
public void Update(bool ignoreMergeFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | Si`verdadero` luego se abandona el formato de resultado de campo directo, independientemente del modificador MERGEFORMAT; de lo contrario, se realiza una actualización normal. |

### Ejemplos

Muestra cómo conservar o descartar campos INCLUDEPICTURE al cargar un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Podemos establecer una bandera en un objeto LoadOptions para decidir si convertir todos los campos INCLUDEPICTURE
    // en formas de imagen al cargar un documento que las contiene.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../field/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
