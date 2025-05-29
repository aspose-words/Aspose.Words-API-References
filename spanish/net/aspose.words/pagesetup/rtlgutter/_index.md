---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PageSetup RtlGutter de Microsoft Word optimiza el diseño de secciones para idiomas de derecha a izquierda y de izquierda a derecha. ¡Mejore el diseño de sus documentos!
type: docs
weight: 380
url: /es/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Obtiene o establece si Microsoft Word utiliza márgenes para la sección en función de un idioma de derecha a izquierda o de izquierda a derecha.

```csharp
public bool RtlGutter { get; set; }
```

## Ejemplos

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

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
