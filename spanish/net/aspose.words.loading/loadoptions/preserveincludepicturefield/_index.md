---
title: LoadOptions.PreserveIncludePictureField
second_title: Referencia de API de Aspose.Words para .NET
description: LoadOptions propiedad. Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false.
type: docs
weight: 120
url: /es/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false.

```csharp
public bool PreserveIncludePictureField { get; set; }
```

### Observaciones

De forma predeterminada, el campo INCLUDEPICTURE se convierte en un objeto de forma. Puede anular eso si necesita el campo a conservar, por ejemplo, si desea actualizarlo mediante programación. Sin embargo, tenga en cuenta que este enfoque no es común para Aspose.Words. Úselo bajo su propio riesgo.

Uno de los posibles casos de uso puede ser usar un MERGEFIELD como campo secundario para cambiar dinámicamente la ruta de origen de la imagen. En este caso, necesita que INCLUDEPICTURE se conserve en el modelo.

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

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)


