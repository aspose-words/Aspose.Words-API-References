---
title: Enum MergeFieldImageDimensionUnit
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.MergeFieldImageDimensionUnit enumeración. Especifica una unidad de una dimensión de imagen es decir el ancho o el alto utilizada en un proceso de combinación de correspondencia.
type: docs
weight: 2580
url: /es/net/aspose.words.fields/mergefieldimagedimensionunit/
---
## MergeFieldImageDimensionUnit enumeration

Especifica una unidad de una dimensión de imagen (es decir, el ancho o el alto) utilizada en un proceso de combinación de correspondencia.

```csharp
public enum MergeFieldImageDimensionUnit
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Point | `0` | El punto (es decir, 1/72 de pulgada). |
| Percent | `1` | El porcentaje del valor de la dimensión de la imagen original. |

### Ejemplos

Muestra cómo establecer las dimensiones de las imágenes tal como las acepta MERGEFIELDS durante una combinación de correspondencia.

```csharp
{
    Document doc = new Document();

    // Inserte un MERGEFIELD que aceptará imágenes de una fuente durante una combinación de correspondencia. Use el código de campo para hacer referencia
    // una columna en la fuente de datos que contiene los nombres de archivo del sistema local de las imágenes que deseamos usar en la combinación de correspondencia.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // La fuente de datos debe tener una columna de este tipo denominada "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Crear una fuente de datos adecuada.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configure una devolución de llamada para modificar los tamaños de las imágenes en el momento de la combinación, luego ejecute la combinación de correspondencia.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Establece el tamaño de todas las imágenes combinadas de correo a un ancho y alto definidos.
/// </summary>
private class MergedImageResizer : IFieldMergingCallback
{
    public MergedImageResizer(double imageWidth, double imageHeight, MergeFieldImageDimensionUnit unit)
    {
        mImageWidth = imageWidth;
        mImageHeight = imageHeight;
        mUnit = unit;
    }

    public void FieldMerging(FieldMergingArgs e)
    {
        throw new NotImplementedException();
    }

    public void ImageFieldMerging(ImageFieldMergingArgs args)
    {
        args.ImageFileName = args.FieldValue.ToString();
        args.ImageWidth = new MergeFieldImageDimension(mImageWidth, mUnit);
        args.ImageHeight = new MergeFieldImageDimension(mImageHeight, mUnit);

        Assert.AreEqual(mImageWidth, args.ImageWidth.Value);
        Assert.AreEqual(mUnit, args.ImageWidth.Unit);
        Assert.AreEqual(mImageHeight, args.ImageHeight.Value);
        Assert.AreEqual(mUnit, args.ImageHeight.Unit);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


