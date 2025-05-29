---
title: PageSetup.DifferentFirstPageHeaderFooter
linktitle: DifferentFirstPageHeaderFooter
articleTitle: DifferentFirstPageHeaderFooter
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageSetup DifferentFirstPageHeaderFooter para personalizar la primera página de su documento con encabezados y pies de página únicos para un toque profesional.
type: docs
weight: 110
url: /es/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

Verdadero si se utiliza un encabezado o pie de página diferente en la primera página.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

## Ejemplos

Muestra cómo crear encabezados y pies de página en un documento utilizando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Especificamos que queremos encabezados y pies de página diferentes para la primera página, páginas pares e impares.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Cree los encabezados y luego agregue tres páginas al documento para mostrar cada tipo de encabezado.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Muestra cómo habilitar o deshabilitar encabezados y pies de página principales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos tipos de encabezado/pie de página.
// 1 - El encabezado/pie de página "Primero", que aparece en la primera página de la sección.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 - El encabezado/pie de página "Principal", que aparece en todas las páginas de la sección.
//Podemos anular el encabezado/pie de página principal con un primer encabezado/pie de página y uno de página par.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Cada sección tiene un objeto "PageSetup" que especifica propiedades relacionadas con la apariencia de la página
// como orientación, tamaño y bordes.
// Establezca la propiedad "DifferentFirstPageHeaderFooter" en "true" para aplicar el primer encabezado/pie de página a la primera página.
// Establezca la propiedad "DifferentFirstPageHeaderFooter" en "falso"
// para hacer que la primera página muestre el encabezado/pie de página principal.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

Muestra cómo rastrear el orden en que una operación de reemplazo de texto recorre los nodos.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // El uso de un encabezado/pie de página diferente para la primera página afectará el orden de búsqueda.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Durante una operación de búsqueda y reemplazo, registra el contenido de cada nodo que tenga texto que la operación "encuentra".
/// en el estado en que se encontraba antes de que se realizara el reemplazo.
/// Esto mostrará el orden en que la operación de reemplazo de texto recorre los nodos.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
