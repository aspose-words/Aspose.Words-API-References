---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.FillType para mejorar sus objetos rellenables con tipos de relleno versátiles para un mejor diseño del documento.
type: docs
weight: 1280
url: /es/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Especifica el tipo de relleno para un objeto rellenable.

```csharp
public enum FillType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Solid | `1` | Relleno sólido. |
| Patterned | `2` | Relleno estampado. |
| Gradient | `3` | Relleno degradado. |
| Textured | `4` | Relleno texturizado. |
| Background | `5` | El relleno es el mismo que el fondo. |
| Picture | `6` | Relleno de imagen. |

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

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
