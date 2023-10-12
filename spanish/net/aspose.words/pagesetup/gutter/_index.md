---
title: PageSetup.Gutter
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Obtiene o establece la cantidad de espacio adicional agregado al margen para la encuadernación del documento.
type: docs
weight: 160
url: /es/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Obtiene o establece la cantidad de espacio adicional agregado al margen para la encuadernación del documento.

```csharp
public double Gutter { get; set; }
```

### Ejemplos

Muestra cómo configurar un documento que se puede imprimir como un pliegue de libro.

```csharp
Document doc = new Document();

// Inserta texto que abarque 16 páginas.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de libro.
// Cuando imprimimos este documento por ambas caras, podemos tomar las páginas para apilarlas
// y dóblalos todos por la mitad a la vez. El contenido del documento se alineará formando un pliegue de libro.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Sólo podemos especificar el número de hojas en múltiplos de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Muestra cómo configurar los márgenes del medianil.

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

// Determina cuánto espacio tienen nuestras páginas para el texto dentro de los márgenes y luego agrega una cantidad para rellenar un margen.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Establece la propiedad "RtlGutter" en "true" para colocar el medianil en una posición más adecuada para texto de derecha a izquierda.
pageSetup.RtlGutter = true;

// Establece la propiedad "MultiplePages" en "MultiplePagesType.MirrorMargins" para alternar
// la posición del lado izquierdo/derecho de los márgenes de cada página.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


