---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words para .NET
description: Controle el campo INCLUDEPICTURE en formatos de Microsoft Word con LoadOptions PreserveIncludePictureField. Administre fácilmente el formato del documento para obtener resultados óptimos.
type: docs
weight: 120
url: /es/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es`FALSO` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Observaciones

De forma predeterminada, el campo INCLUDEPICTURE se convierte en un objeto de forma. Puede anular esta configuración si necesita que el campo se conserve, por ejemplo, si desea actualizarlo mediante programación. Sin embargo, tenga en cuenta que este método no es común en Aspose.Words. Úselo bajo su propia responsabilidad.

Un posible caso de uso podría ser usar un MERGEFIELD como campo secundario para cambiar dinámicamente la ruta de origen de la imagen. En este caso, es necesario conservar INCLUDEPICTURE en el modelo.

## Ejemplos

Muestra cómo conservar o descartar los campos INCLUDEPICTURE al cargar un documento.

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
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
