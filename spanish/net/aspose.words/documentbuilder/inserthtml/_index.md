---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words para .NET
description: Mejore sin esfuerzo sus documentos con el método InsertHtml de DocumentBuilder: inserte sin problemas cadenas HTML para una integración de contenido dinámico.
type: docs
weight: 380
url: /es/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

Inserta una cadena HTML en el documento.

```csharp
public void InsertHtml(string html)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| html | String | Una cadena HTML para insertar en el documento. |

## Observaciones

Puede utilizar este método para insertar un fragmento HTML o un documento HTML completo.

## Ejemplos

Muestra cómo utilizar un generador de documentos para insertar contenido HTML en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// Al insertar código HTML se analiza el formato de cada elemento en el formato de texto del documento equivalente.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

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

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

Inserta una cadena HTML en el documento.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| html | String | Una cadena HTML para insertar en el documento. |
| useBuilderFormatting | Boolean | Un valor que indica si el formato especificado en[`DocumentBuilder`](../) se utiliza como formato base para el texto importado desde HTML. |

## Observaciones

Puede utilizar este método para insertar un fragmento HTML o un documento HTML completo.

Cuando*useBuilderFormatting* es`FALSO` , [`DocumentBuilder`](../) Se ignora el formato y el texto insertado se formatea según el formato HTML predeterminado. Como resultado, el texto se ve tal como se muestra en los navegadores.

Cuando*useBuilderFormatting* es`verdadero` El formato , del texto insertado se basa en[`DocumentBuilder`](../) formato, y el texto parece como si se hubiera insertado con[`Write`](../write/) .

## Ejemplos

Muestra cómo aplicar el formato de un generador de documentos al insertar contenido HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca una alineación de texto para el constructor, inserte un párrafo HTML con una alineación especificada y uno sin ella.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

El primer párrafo tiene una alineación especificada. Cuando InsertHtml analiza el código HTML,
// El valor de alineación del párrafo que se encuentra en el código HTML siempre reemplaza el valor del generador de documentos.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

El segundo párrafo no tiene alineación especificada. Se puede completar su valor de alineación.
// por el valor del constructor dependiendo de la bandera que pasamos al método InsertHtml.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

Inserta una cadena HTML en el documento. Permite especificar opciones adicionales.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| html | String | Una cadena HTML para insertar en el documento. |
| options | HtmlInsertOptions | Opciones que se utilizan cuando se inserta una cadena HTML. |

## Observaciones

Puede utilizar este método para insertar un fragmento HTML o un documento HTML completo.

## Ejemplos

Muestra cómo utilizar opciones al insertar HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// De forma predeterminada, "DocumentBuilder.InsertHtml" inserta un fragmento HTML que termina con un elemento HTML a nivel de bloque,
// Normalmente cierra ese elemento de nivel de bloque e inserta un salto de párrafo.
// Como resultado, aparece un nuevo párrafo vacío después del documento insertado.
// Si especificamos "HtmlInsertOptions.RemoveLastEmptyParagraph", se eliminarán esos párrafos vacíos adicionales.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Ver también

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
