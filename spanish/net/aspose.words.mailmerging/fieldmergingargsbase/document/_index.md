---
title: FieldMergingArgsBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldMergingArgsBase Document, que proporciona el objeto Document para operaciones de combinación de correspondencia fluidas. ¡Mejore su flujo de trabajo hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/fieldmergingargsbase/document/
---
## FieldMergingArgsBase.Document property

Devuelve el`Document`objeto para el cual se realiza la combinación de correspondencia.

```csharp
public Document Document { get; }
```

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
/// esta devolución de llamada analiza sus datos de combinación como contenido HTML y agrega el resultado a la ubicación del documento MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Se llama cuando una combinación de correspondencia fusiona datos en un MERGEFIELD.
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
        //No hacer nada.
    }
}
```

### Ver también

* class [Document](../../../aspose.words/document/)
* class [FieldMergingArgsBase](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
