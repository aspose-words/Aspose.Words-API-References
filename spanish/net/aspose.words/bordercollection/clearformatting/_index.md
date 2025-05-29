---
title: BorderCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: Descubra cómo el método ClearFormatting de BorderCollection elimina sin esfuerzo todos los bordes de los objetos, mejorando su diseño con imágenes limpias y nítidas.
type: docs
weight: 140
url: /es/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

Elimina todos los bordes de un objeto.

```csharp
public void ClearFormatting()
```

## Ejemplos

Muestra cómo eliminar todos los bordes de todos los párrafos de un documento.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

//El primer párrafo de este documento tiene bordes visibles con estas configuraciones.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// Utilice el método "ClearFormatting" en cada párrafo para eliminar todos los bordes.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### Ver también

* class [BorderCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
