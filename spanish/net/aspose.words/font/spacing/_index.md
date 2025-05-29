---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words para .NET
description: Descubra la propiedad Espaciado de Fuente para ajustar fácilmente el espaciado entre caracteres en puntos. Mejore la legibilidad y el diseño con un control tipográfico preciso.
type: docs
weight: 390
url: /es/net/aspose.words/font/spacing/
---
## Font.Spacing property

Devuelve o establece el espaciado (en puntos) entre caracteres.

```csharp
public double Spacing { get; set; }
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
