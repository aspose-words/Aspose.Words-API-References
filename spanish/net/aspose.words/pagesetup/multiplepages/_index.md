---
title: PageSetup.MultiplePages
linktitle: MultiplePages
articleTitle: MultiplePages
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PageSetup MultiplePages optimiza la impresión de documentos para una encuadernación impecable. ¡Mejore sus documentos de varias páginas hoy mismo!
type: docs
weight: 270
url: /es/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

Para documentos de varias páginas, obtiene o establece cómo se imprime o representa un documento para que pueda encuadernarse como un folleto.

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

## Ejemplos

Muestra cómo configurar un documento que se puede imprimir como un libro plegable.

```csharp
Document doc = new Document();

// Insertar texto que abarca 16 páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de libro plegable.
// Cuando imprimimos este documento por ambas caras, podemos tomar las páginas para apilarlas
// y dóblalos todos por la mitad a la vez. El contenido del documento se alineará formando un pliegue.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

//Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Muestra cómo establecer márgenes de canal.

```csharp
Document doc = new Document();

// Insertar texto que abarque varias páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Un canal agrega espacios en blanco al margen izquierdo o derecho de la página.
// lo que compensa el plegado central de las páginas de un libro que invade el diseño de la página.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Determine cuánto espacio tienen nuestras páginas para el texto dentro de los márgenes y luego agregue una cantidad para rellenar un margen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Establezca la propiedad "RtlGutter" en "true" para colocar el margen en una posición más adecuada para el texto de derecha a izquierda.
pageSetup.RtlGutter = true;

// Establezca la propiedad "MultiplePages" en "MultiplePagesType.MirrorMargins" para alternar
// la posición de los márgenes del lado izquierdo/derecho de cada página.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Ver también

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
