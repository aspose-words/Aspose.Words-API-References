---
title: Class MergeFieldImageDimension
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.MergeFieldImageDimension clase. Representa una dimensión de la imagen es decir el ancho o el alto utilizada en un proceso de combinación de correspondencia.
type: docs
weight: 2570
url: /es/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Representa una dimensión de la imagen (es decir, el ancho o el alto) utilizada en un proceso de combinación de correspondencia.

```csharp
public class MergeFieldImageDimension
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(double) | Crea una instancia de dimensión de imagen con el valor dado en puntos. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(double, MergeFieldImageDimensionUnit) | Crea una instancia de dimensión de imagen con el valor dado y la unidad dada. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | La unidad. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | El valor. |

### Observaciones

Para indicar que la imagen debe insertarse con su dimensión original durante una combinación de correo, debe asignar un valor negativo a la[`Value`](./value/) propiedad.

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


