---
title: FieldToc.PageNumberOmittingLevelRange
linktitle: PageNumberOmittingLevelRange
articleTitle: PageNumberOmittingLevelRange
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldToc PageNumberOmittingLevelRange para personalizar su tabla de contenido omitiendo números de página para niveles de entrada específicos.
type: docs
weight: 110
url: /es/net/aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/
---
## FieldToc.PageNumberOmittingLevelRange property

Obtiene o establece un rango de niveles de las entradas de la tabla de contenido desde donde se omiten los números de página.

```csharp
public string PageNumberOmittingLevelRange { get; set; }
```

## Ejemplos

Muestra cómo insertar una tabla de contenido y rellenarla con entradas basadas en estilos de encabezado.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Inserte un campo TOC, que compilará todos los encabezados en una tabla de contenido.
    // Para cada encabezado, este campo creará una línea con el texto en ese estilo de encabezado a la izquierda,
    // y la página en la que aparece el encabezado aparece a la derecha.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Utilice la propiedad BookmarkName para enumerar únicamente los encabezados
    // que aparecen dentro de los límites de un marcador con el nombre "MiMarcador".
    field.BookmarkName = "MyBookmark";

    // El texto con un estilo de encabezado incorporado, como "Encabezado 1", aplicado, contará como un encabezado.
    //Podemos nombrar estilos adicionales para que sean seleccionados como encabezados por la TOC en esta propiedad y sus niveles de TOC.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // De forma predeterminada, los niveles de Estilos/TOC están separados en la propiedad CustomStyles por una coma,
    // pero podemos establecer un delimitador personalizado en esta propiedad.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configure el campo para excluir cualquier encabezado que tenga niveles de TOC fuera de este rango.
    field.HeadingLevelRange = "1-3";

    // La tabla de contenidos no mostrará los números de página de los encabezados cuyos niveles de tabla de contenidos estén dentro de este rango.
    field.PageNumberOmittingLevelRange = "2-5";

     // Establezca una cadena personalizada que separará cada encabezado de su número de página.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Estos dos encabezados tendrán los números de página omitidos porque están dentro del rango "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    //Esta entrada no aparece porque "Título 4" está fuera del rango "1-3" que hemos establecido anteriormente.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    //Esta entrada no aparece porque está fuera del marcador especificado por la tabla de contenidos.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Iniciar una nueva página e insertar un párrafo de un estilo específico.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Ver también

* class [FieldToc](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
