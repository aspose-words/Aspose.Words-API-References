---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words para .NET
description: Descubra la propiedad Color de relleno para personalizar fácilmente el color de primer plano de su diseño con un objeto Color, mejorando el atractivo visual de su proyecto.
type: docs
weight: 50
url: /es/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

Obtiene o establece un objeto Color que representa el color de primer plano para el relleno.

```csharp
public Color Color { get; set; }
```

## Observaciones

Esta propiedad conserva el componente alfa de laColor , a diferencia de la[`ForeColor`](../forecolor/) propiedad, que lo restablece a un color completamente opaco.

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

* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
