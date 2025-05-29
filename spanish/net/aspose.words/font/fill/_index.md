---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words para .NET
description: Descubra la propiedad Relleno de fuente para mejorar la apariencia de su texto con un formato de relleno personalizable para una apariencia pulida y profesional.
type: docs
weight: 130
url: /es/net/aspose.words/font/fill/
---
## Font.Fill property

Obtiene el formato de relleno para el[`Font`](../) .

```csharp
public Fill Fill { get; }
```

## Ejemplos

Muestra cómo convertir cualquiera de los rellenos nuevamente a relleno sólido.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtener el objeto de relleno para la fuente de la primera ejecución.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Verificar las propiedades de relleno de la fuente.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia el tipo de relleno a Sólido con color verde uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Ver también

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
