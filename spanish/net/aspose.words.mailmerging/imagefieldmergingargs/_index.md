---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: Aspose.Words para .NET
description: Aspose.Words.MailMerging.ImageFieldMergingArgs clase. Proporciona datos para elImageFieldMerging evento en C#.
type: docs
weight: 3830
url: /es/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Proporciona datos para el[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) evento.

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) artículo de documentación.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Devuelve el[`Document`](../fieldmergingargsbase/document/) objeto para el cual se realiza la combinación de correspondencia. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Obtiene el nombre del campo de combinación tal como se especifica en el documento. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Obtiene el objeto que representa el campo de combinación actual. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Obtiene el nombre del campo de combinación en la fuente de datos. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Obtiene o establece el valor del campo del origen de datos. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Especifica la imagen que el motor de combinación de correspondencia debe insertar en el documento. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Establece el nombre de archivo de la imagen que el motor de combinación de correspondencia debe insertar en el documento. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Especifica la altura de la imagen para insertarla en el documento. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Especifica la secuencia para que el motor de combinación de correspondencia lea una imagen. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Especifica el ancho de la imagen para insertarla en el documento. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Obtiene el índice de base cero del registro que se está fusionando. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Especifica la forma que el motor de combinación de correspondencia debe insertar en el documento. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Obtiene el nombre de la tabla de datos para la operación de combinación actual o una cadena vacía si el nombre no está disponible. |

## Observaciones

Este evento ocurre durante la combinación de correspondencia cuando se encuentra un campo de imagen mail merge en el documento. Puede responder a este evento para devolver un nombre de archivo, secuencia o un archivo .Image objeto al motor mail merge para que se inserte en el documento.

Hay tres propiedades disponibles.[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) y[`Image`](./image/) para especificar de dónde se debe tomar la imagen. Establezca solo una de estas propiedades.

Para insertar un campo de combinación de correspondencia de imagen en un documento en Word, seleccione el comando Insertar/Campo, , luego seleccione MergeField y escriba Imagen:MyFieldName.

## Ejemplos

Muestra cómo insertar imágenes almacenadas en un campo BLOB de la base de datos en un informe.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Abra el lector de datos, que debe estar en un modo que lea todos los registros a la vez.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hacer nada.
    }

    /// <summary>
    /// Esto se llama cuando una combinación de correspondencia encuentra un MERGEFIELD en el documento con una etiqueta "Imagen:" en su nombre.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Muestra cómo configurar las dimensiones de las imágenes según las acepta MERGEFIELDS durante una combinación de correspondencia.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Inserte un MERGEFIELD que acepte imágenes de una fuente durante una combinación de correspondencia. Utilice el código de campo para hacer referencia
    // una columna en la fuente de datos que contiene los nombres de archivos del sistema local de las imágenes que deseamos usar en la combinación de correspondencia.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // La fuente de datos debe tener una columna llamada "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Crea una fuente de datos adecuada.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Configure una devolución de llamada para modificar los tamaños de las imágenes en el momento de la combinación y luego ejecute la combinación de correspondencia.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Establece el tamaño de todas las imágenes combinadas por correo en un ancho y alto definidos.
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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
