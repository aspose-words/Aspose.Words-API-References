---
title: FieldMergingArgsBase Class
linktitle: FieldMergingArgsBase
articleTitle: FieldMergingArgsBase
second_title: Aspose.Words para .NET
description: Aspose.Words.MailMerging.FieldMergingArgsBase clase. Clase base paraFieldMergingArgs yImageFieldMergingArgs  en C#.
type: docs
weight: 3780
url: /es/net/aspose.words.mailmerging/fieldmergingargsbase/
---
## FieldMergingArgsBase class

Clase base para[`FieldMergingArgs`](../fieldmergingargs/) y[`ImageFieldMergingArgs`](../imagefieldmergingargs/) .

Para obtener más información, visite el[Combinación de correspondencia e informes](https://docs.aspose.com/words/net/mail-merge-and-reporting/) artículo de documentación.

```csharp
public abstract class FieldMergingArgsBase
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Devuelve el[`Document`](./document/) objeto para el cual se realiza la combinación de correspondencia. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Obtiene el nombre del campo de combinación tal como se especifica en el documento. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Obtiene el objeto que representa el campo de combinación actual. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Obtiene el nombre del campo de combinación en la fuente de datos. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Obtiene o establece el valor del campo del origen de datos. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Obtiene el índice de base cero del registro que se está fusionando. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Obtiene el nombre de la tabla de datos para la operación de combinación actual o una cadena vacía si el nombre no está disponible. |

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con una devolución de llamada personalizada que maneja datos combinados en forma de documentos HTML.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Si la combinación de correspondencia encuentra un MERGEFIELD cuyo nombre comienza con el prefijo "html_",
/// esta devolución de llamada analiza sus datos combinados como contenido HTML y agrega el resultado a la ubicación del documento de MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Se llama cuando una combinación de correspondencia combina datos en un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Agrega datos HTML analizados al cuerpo del documento.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Como ya hemos insertado el contenido fusionado manualmente,
             // no necesitaremos responder a este evento devolviendo contenido a través de la propiedad "Texto".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hacer nada.
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
