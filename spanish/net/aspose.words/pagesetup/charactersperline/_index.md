---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words para .NET
description: PageSetup CharactersPerLine propiedad. Obtiene o establece el número de caracteres por línea en la cuadrícula del documento en C#.
type: docs
weight: 100
url: /es/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Obtiene o establece el número de caracteres por línea en la cuadrícula del documento.

```csharp
public int CharactersPerLine { get; set; }
```

## Observaciones

El valor mínimo de la propiedad es 1. El valor máximo depende del ancho de la página y del tamaño de fuente del estilo Normal . El paso mínimo de los caracteres es el 90 por ciento del tamaño de fuente. Por ejemplo, el número máximo de caracteres por línea de una página Carta con márgenes de una pulgada es 43.

De forma predeterminada, la propiedad tiene un valor en el que el paso de los caracteres es igual al tamaño de fuente del estilo Normal .

## Ejemplos

Muestra cómo especificar un para el número de caracteres que puede tener cada línea.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Habilite el paso y luego utilícelo para establecer el número de caracteres por línea en esta sección.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// El número de caracteres también depende del tamaño de la fuente.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
