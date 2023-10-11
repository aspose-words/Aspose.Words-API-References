---
title: Border.ClearFormatting
second_title: Referencia de API de Aspose.Words para .NET
description: Border método. Restablece las propiedades del borde a los valores predeterminados.
type: docs
weight: 90
url: /es/net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

Restablece las propiedades del borde a los valores predeterminados.

```csharp
public void ClearFormatting()
```

### Observaciones

Cuando las propiedades del borde se restablecen a los valores predeterminados, el borde es invisible.

### Ejemplos

Muestra cómo eliminar bordes de un párrafo.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// Cada párrafo tiene un conjunto individual de bordes.
// Podemos acceder a la configuración para la apariencia de estos bordes a través del objeto de formato de párrafo.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 // Podemos eliminar un borde de inmediato ejecutando el método ClearFormatting.
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
* espacio de nombres [Aspose.Words](../../border/)
* asamblea [Aspose.Words](../../../)


