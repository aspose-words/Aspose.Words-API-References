---
title: Border.IsVisible
linktitle: IsVisible
articleTitle: IsVisible
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad Border IsVisible mejora su diseño al devolver el valor "true" al aplicar LineStyle. ¡Optimice su interfaz de usuario con esta función clave!
type: docs
weight: 30
url: /es/net/aspose.words/border/isvisible/
---
## Border.IsVisible property

Devuelve`verdadero` Si el[`LineStyle`](../linestyle/) no esNone .

```csharp
public bool IsVisible { get; }
```

## Ejemplos

Muestra cómo eliminar los bordes de un párrafo.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

//Cada párrafo tiene un conjunto individual de bordes.
//Podemos acceder a la configuración de la apariencia de estos bordes a través del objeto de formato de párrafo.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 //Podemos eliminar un borde de una vez ejecutando el método ClearFormatting.
// Ejecutar este método en cada borde de un párrafo eliminará todos sus bordes.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### Ver también

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
