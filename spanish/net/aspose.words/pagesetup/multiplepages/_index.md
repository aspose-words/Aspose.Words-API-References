---
title: PageSetup.MultiplePages
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Para documentos de varias páginas obtiene o establece cómo se imprime o procesa un documento para que pueda encuadernarse como un folleto.
type: docs
weight: 260
url: /es/net/aspose.words/pagesetup/multiplepages/
---
## PageSetup.MultiplePages property

Para documentos de varias páginas, obtiene o establece cómo se imprime o procesa un documento para que pueda encuadernarse como un folleto.

```csharp
public MultiplePagesType MultiplePages { get; set; }
```

### Ejemplos

Muestra cómo configurar un documento que se puede imprimir como un pliegue de libro.

```csharp
Document doc = new Document();

// Insertar texto que abarque 16 páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de un pliegue de libro.
// Cuando imprimimos este documento por ambos lados, podemos tomar las páginas para apilarlas
// y doblarlos todos por la mitad a la vez. El contenido del documento se alineará en un pliegue de libro.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Muestra cómo configurar los márgenes de medianil.

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

// Un medianil agrega espacios en blanco al margen izquierdo o derecho de la página,
// que compensa el plegado central de las páginas de un libro que invade el diseño de la página.
PageSetup pageSetup = doc.Sections[0].PageSetup;

  // Determine cuánto espacio tienen nuestras páginas para el texto dentro de los márgenes y luego agregue una cantidad para rellenar un margen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Establezca la propiedad "RtlGutter" en "true" para colocar la medianil en una posición más adecuada para el texto de derecha a izquierda.
pageSetup.RtlGutter = true;

// Establecer la propiedad "MultiplePages" en "MultiplePagesType.MirrorMargins" para alternar
// la posición del lado izquierdo/derecho de la página de los márgenes de cada página.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Ver también

* enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


