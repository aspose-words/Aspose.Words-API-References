---
title: Border.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words para .NET
description: Descubre el método "Borde Igual" para comparar fácilmente los valores de los bordes y mejorar la precisión de tu diseño. ¡Consigue resultados consistentes sin esfuerzo!
type: docs
weight: 100
url: /es/net/aspose.words/border/equals/
---
## Equals(*[Border](../)*) {#equals}

Determina si el borde especificado tiene el mismo valor que el borde actual.

```csharp
public bool Equals(Border rhs)
```

## Ejemplos

Muestra cómo las colecciones de bordes pueden compartir elementos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Dado que utilizamos la misma configuración de borde al crear
// estos párrafos, sus colecciones de bordes comparten los mismos elementos.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

//Después de cambiar el estilo de línea de los bordes solo en el segundo párrafo,
//Las colecciones de borde ya no comparten los mismos elementos.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    //Cambiar la apariencia de un borde vacío lo hace visible.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Ver también

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Determina si el objeto especificado es igual en valor al objeto actual.

```csharp
public override bool Equals(object obj)
```

## Ejemplos

Muestra cómo las colecciones de bordes pueden compartir elementos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Write("Paragraph 2.");

// Dado que utilizamos la misma configuración de borde al crear
// estos párrafos, sus colecciones de bordes comparten los mismos elementos.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
BorderCollection secondParagraphBorders = builder.CurrentParagraph.ParagraphFormat.Borders;
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsTrue(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());
    Assert.False(firstParagraphBorders[i].IsVisible);
}

foreach (Border border in secondParagraphBorders)
    border.LineStyle = LineStyle.DotDash;

//Después de cambiar el estilo de línea de los bordes solo en el segundo párrafo,
//Las colecciones de borde ya no comparten los mismos elementos.
for (int i = 0; i < firstParagraphBorders.Count; i++)
{
    Assert.IsFalse(firstParagraphBorders[i].Equals(secondParagraphBorders[i]));
    Assert.AreNotEqual(firstParagraphBorders[i].GetHashCode(), secondParagraphBorders[i].GetHashCode());

    //Cambiar la apariencia de un borde vacío lo hace visible.
    Assert.True(secondParagraphBorders[i].IsVisible);
}

doc.Save(ArtifactsDir + "Border.SharedElements.docx");
```

### Ver también

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
