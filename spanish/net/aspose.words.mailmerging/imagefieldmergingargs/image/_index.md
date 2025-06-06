---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar ImageFieldMergingArgs para insertar imágenes sin problemas en sus documentos y disfrutar de una experiencia de combinación de correspondencia impecable.
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Especifica la imagen que el motor de combinación de correspondencia debe insertar en el documento.

```csharp
public Image Image { get; set; }
```

## Ejemplos

Muestra cómo utilizar una devolución de llamada para personalizar la lógica de fusión de imágenes.

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // Inserte un MERGEFIELD que acepte imágenes de una fuente durante la combinación de correspondencia. Use el código de campo para hacer referencia.
    // una columna en la fuente de datos que contiene los nombres de archivos del sistema local de las imágenes que deseamos usar en la combinación de correspondencia.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // En este caso, el campo espera que la fuente de datos tenga una columna llamada "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Los nombres de archivos pueden ser largos y, si podemos encontrar una forma de evitar almacenarlos en la fuente de datos,
    //podemos reducir considerablemente su tamaño.
    // Crea una fuente de datos que haga referencia a imágenes usando nombres cortos.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Asignar una devolución de llamada de fusión que contenga toda la lógica que procesa esos nombres,
     // y luego ejecutar la combinación de correspondencia.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// Contiene un diccionario que asigna nombres de imágenes a nombres de archivos del sistema local que contienen estas imágenes.
/// Si una fuente de datos de combinación de correspondencia utiliza uno de los nombres del diccionario para referirse a una imagen,
/// esta devolución de llamada pasará el nombre de archivo respectivo al destino de la fusión.
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET461_OR_GREATER || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### Ver también

* class [ImageFieldMergingArgs](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
