---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words para .NET
description: Descubra cómo personalizar fácilmente la configuración de fuentes de sus documentos. Mejore sus documentos con opciones de fuente personalizadas para una mejor legibilidad y estilo.
type: docs
weight: 150
url: /es/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Obtiene o establece la configuración de fuente del documento.

```csharp
public FontSettings FontSettings { get; set; }
```

## Observaciones

Esta propiedad permite especificar la configuración de fuentes por documento. Si se establece en`nulo` , configuración de fuente estática predeterminada [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) se utilizará.

El valor predeterminado es`nulo`.

## Ejemplos

Muestra cómo establecer reglas de sustitución de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Las fuentes de fuentes predeterminadas contienen la primera fuente que utiliza el documento.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

//La segunda fuente, "Amethysta", no está disponible.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

//Podemos configurar una tabla de sustitución de fuentes que determine
// qué fuentes utilizará Aspose.Words como sustitutas de las fuentes no disponibles.
// Establezca dos fuentes de sustitución para "Amethysta": "Arvo" y "Courier New".
// Si el primer sustituto no está disponible, Aspose.Words intenta utilizar el segundo sustituto, y así sucesivamente.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" no está disponible y la regla de sustitución establece que la primera fuente a utilizar como sustituta es "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" tampoco está disponible, pero "Courier New" sí.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

//El documento de salida mostrará el texto que utiliza la fuente "Amethysta" formateada con "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Ver también

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
