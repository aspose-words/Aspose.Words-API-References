---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words para .NET
description: Descubra cómo configurar eficazmente la propiedad FillType y mejorar su diseño con opciones de relleno personalizables para un mejor impacto visual.
type: docs
weight: 60
url: /es/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

Obtiene un tipo de relleno.

```csharp
public FillType FillType { get; }
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

* enum [FillType](../../filltype/)
* class [Fill](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
