---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words para .NET
description: Font AutoColor propiedad. Devuelve el color calculado actual del texto blanco o negro que se utilizará para el color automático. Si el color no es automático devuelveColor  en C#.
type: docs
weight: 20
url: /es/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Devuelve el color calculado actual del texto (blanco o negro) que se utilizará para el 'color automático'. Si el color no es 'automático', devuelve[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Observaciones

Cuando el texto tiene 'color automático', el color real del texto se calcula automáticamente para que sea legible contra el color de fondo. A medida que cambia el color de fondo, el color del texto cambiará automáticamente a blanco o negro en MS Word para maximizar la legibilidad.

## Ejemplos

Muestra cómo mejorar la legibilidad seleccionando automáticamente el color del texto según el brillo de su fondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si el objeto Fuente de una ejecución no especifica el color del texto, automáticamente
// seleccione blanco o negro según el color del fondo.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// El color predeterminado del texto es negro. Si el color del fondo es oscuro, será difícil ver el texto negro.
// Para solucionar este problema, la propiedad AutoColor mostrará este texto en blanco.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Si cambiamos el fondo a un color claro, el negro será más
// color de texto adecuado que el blanco para que el color automático lo muestre en negro.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
