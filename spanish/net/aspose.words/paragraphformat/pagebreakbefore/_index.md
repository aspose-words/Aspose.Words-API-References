---
title: ParagraphFormat.PageBreakBefore
linktitle: PageBreakBefore
articleTitle: PageBreakBefore
second_title: Aspose.Words para .NET
description: ParagraphFormat PageBreakBefore propiedad. Verdadero si se fuerza un salto de página antes del párrafo en C#.
type: docs
weight: 260
url: /es/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Verdadero si se fuerza un salto de página antes del párrafo.

```csharp
public bool PageBreakBefore { get; set; }
```

## Ejemplos

Muestra cómo crear párrafos con saltos de página al principio.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establece esta bandera en "verdadero" para aplicar un salto de página al comienzo de cada párrafo
// que el creador de documentos creará bajo esta configuración de ParagraphFormat.
// El primer párrafo no recibirá un salto de página.
// Deja esta bandera como "falso" para comenzar cada nuevo párrafo en la misma página
// como el anterior, siempre que haya suficiente espacio.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(2, layoutCollector.GetStartPageIndex(paragraphs[1]));
}
else
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[1]));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
