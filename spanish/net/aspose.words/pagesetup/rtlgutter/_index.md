---
title: PageSetup.RtlGutter
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Obtiene o establece si Microsoft Word usa medianil para la sección en función de un idioma de derecha a izquierda o de izquierda a derecha.
type: docs
weight: 370
url: /es/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Obtiene o establece si Microsoft Word usa medianil para la sección en función de un idioma de derecha a izquierda o de izquierda a derecha.

```csharp
public bool RtlGutter { get; set; }
```

### Ejemplos

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

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


