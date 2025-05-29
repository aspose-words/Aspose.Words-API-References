---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words para .NET
description: Descubre la propiedad AutoColor de Fuente y obtén el color actual del texto (negro o blanco) para ajustes de color automáticos. ¡Optimiza tu diseño fácilmente!
type: docs
weight: 20
url: /es/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Devuelve el color actual calculado del texto (negro o blanco) que se utilizará para 'color automático'. Si el color no es 'automático', devuelve[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Observaciones

Cuando el texto tiene "color automático", el color real del texto se calcula automáticamente para que sea legible sobre el color de fondo. Al cambiar el color de fondo, el color del texto cambiará automáticamente a negro o blanco en MS Word para maximizar la legibilidad.

## Ejemplos

Muestra cómo mejorar la legibilidad seleccionando automáticamente el color del texto en función del brillo de su fondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si el objeto Fuente de una ejecución no especifica el color del texto, se especificará automáticamente.
// seleccione negro o blanco dependiendo del color del fondo.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

El color predeterminado del texto es el negro. Si el color de fondo es oscuro, el texto negro será difícil de ver.
// Para resolver este problema, la propiedad AutoColor mostrará este texto en blanco.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Si cambiamos el fondo a un color claro, el negro será un color más
// color de texto más adecuado que el blanco para que el color automático lo muestre en negro.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
