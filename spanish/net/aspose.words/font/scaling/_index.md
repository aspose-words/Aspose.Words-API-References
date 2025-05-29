---
title: Font.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words para .NET
description: Descubra la propiedad Escala de fuente para ajustar el ancho de los caracteres en porcentaje, mejorando la legibilidad del texto y la flexibilidad de diseño para sus proyectos.
type: docs
weight: 320
url: /es/net/aspose.words/font/scaling/
---
## Font.Scaling property

Obtiene o establece la escala del ancho del carácter en porcentaje.

```csharp
public int Scaling { get; set; }
```

## Ejemplos

Muestra cómo establecer la escala y el espaciado horizontal de los caracteres.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Agrega una tirada de texto y aumenta el ancho del carácter al 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Agregue una secuencia de texto y agregue 1 punto de espacio horizontal adicional entre cada carácter.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Agrega una serie de texto y acerca los caracteres 1 punto.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
