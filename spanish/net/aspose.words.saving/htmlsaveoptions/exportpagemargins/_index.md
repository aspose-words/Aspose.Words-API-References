---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions ExportPageMargins mejora sus exportaciones HTML, MHTML y EPUB al controlar los márgenes de página para una presentación impecable.
type: docs
weight: 210
url: /es/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Especifica si los márgenes de la página se exportan a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Observaciones

Aspose.Words no muestra el área de los márgenes de la página de manera predeterminada. Si algún elemento está total o parcialmente recortado por el borde del documento, el área mostrada se puede ampliar con esta opción.

## Ejemplos

Muestra cómo mostrar objetos fuera de límites en documentos HTML de salida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilice un constructor para insertar una forma sin ajuste.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Los valores de posición de forma negativos pueden colocar la forma fuera de los límites de la página.
// Si exportamos esto a HTML, la forma aparecerá truncada.
shape.Left = -150;

// Al guardar el documento en HTML, podemos pasar un objeto SaveOptions
// para decidir si se debe ajustar la página para mostrar completamente los objetos fuera de los límites.
// Si establecemos el indicador "ExportPageMargins" en "verdadero", la forma será completamente visible en el HTML de salida.
// Si establecemos el indicador "ExportPageMargins" en "falso",
//Nuestro documento mostrará la forma truncada como la veríamos en Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
