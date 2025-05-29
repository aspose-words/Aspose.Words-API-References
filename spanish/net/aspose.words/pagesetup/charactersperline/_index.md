---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words para .NET
description: Controle el diseño de su documento con la propiedad PageSetup CharactersPerLine. Ajuste fácilmente los caracteres por línea para una legibilidad y un diseño óptimos.
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

El valor mínimo de la propiedad es 1. El valor máximo depende del ancho de página y del tamaño de fuente del estilo Normal . El paso mínimo entre caracteres es el 90 % del tamaño de fuente. Por ejemplo, el número máximo de caracteres por línea en una página Carta con márgenes de una pulgada es 43.

De forma predeterminada, la propiedad tiene un valor en el que el paso de caracteres es igual al tamaño de fuente del estilo Normal .

## Ejemplos

Muestra cómo especificar la cantidad de caracteres que puede tener cada línea.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Habilite el paso y luego úselo para establecer la cantidad de caracteres por línea en esta sección.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

//El número de caracteres también depende del tamaño de la fuente.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
