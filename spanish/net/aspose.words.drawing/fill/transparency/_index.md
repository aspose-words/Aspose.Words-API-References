---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words para .NET
description: Ajusta la transparencia del relleno de 0.0 (opaco) a 1.0 (transparente) para personalizar los efectos visuales de tus diseños. ¡Mejora la estética de tu proyecto hoy mismo!
type: docs
weight: 200
url: /es/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

Obtiene o establece el grado de transparencia del relleno especificado como un valor entre 0,0 (opaco) y 1,0 (transparente).

```csharp
public double Transparency { get; set; }
```

## Observaciones

Esta propiedad es lo opuesto a la propiedad[`Opacity`](../opacity/).

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
