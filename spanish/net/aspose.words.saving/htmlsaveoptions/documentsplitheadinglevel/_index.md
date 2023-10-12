---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica el nivel máximo de encabezados en los que dividir el documento. El valor predeterminado es2 .
type: docs
weight: 90
url: /es/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Especifica el nivel máximo de encabezados en los que dividir el documento. El valor predeterminado es`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### Observaciones

Cuando[`DocumentSplitCriteria`](../documentsplitcriteria/) incluyeHeadingParagraph y esta propiedad se establece en un valor de 1 a 9, el documento se dividirá en párrafos formateados con  **Título 1** , **Título 2** , **Título 3**etc. estilos hasta el nivel de título especificado.

Por defecto, sólo **Título 1** y **Título 2** Los párrafos hacen que el documento se divida. Establecer esta propiedad en cero hará que el documento no se divida en absoluto en los párrafos del encabezado.

### Ejemplos

Muestra cómo dividir un documento HTML de salida por encabezados en varias partes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cada párrafo al que le damos formato usando un estilo "Encabezado" puede servir como encabezado.
// Cada encabezado también puede tener un nivel de encabezado, determinado por el número de su estilo de encabezado.
// Los títulos siguientes son de los niveles 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Crea un objeto HtmlSaveOptions y establece el criterio de división en "HeadingParagraph".
// Estos criterios dividirán el documento en párrafos con estilos de "Encabezado" en varios documentos más pequeños,
// y guarde cada documento en un archivo HTML independiente en el sistema de archivos local.
// También estableceremos el nivel máximo de encabezado, que divide el documento en 2.
// Al guardar el documento, se dividirá en los encabezados de los niveles 1 y 2, pero no en los del 3 al 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Nuestro documento tiene cuatro títulos de niveles 1 - 2. Uno de esos títulos no será
// un punto de división ya que está al principio del documento.
// La operación de guardar dividirá nuestro documento en tres lugares, en cuatro documentos más pequeños.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


