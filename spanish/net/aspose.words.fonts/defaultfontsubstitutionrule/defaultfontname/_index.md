---
title: DefaultFontSubstitutionRule.DefaultFontName
second_title: Referencia de API de Aspose.Words para .NET
description: DefaultFontSubstitutionRule propiedad. Obtiene o establece el nombre de fuente predeterminado.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Obtiene o establece el nombre de fuente predeterminado.

```csharp
public string DefaultFontName { get; set; }
```

### Observaciones

El valor predeterminado es 'Times New Roman'.

### Ejemplos

Muestra cómo configurar la regla de sustitución de fuente predeterminada.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Obtenga la regla de sustitución predeterminada dentro de FontSettings.
// Esta regla sustituirá todas las fuentes faltantes con "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Establecer el sustituto de fuente predeterminado en "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Usando un generador de documentos, agregue algo de texto en una fuente que no tengamos que ver que se lleva a cabo la sustitución,
// y luego renderiza el resultado en un PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

Muestra cómo especificar una fuente predeterminada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Las fuentes de fuentes que utiliza el documento contienen la fuente "Arial", pero no "Arvo".
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Establecer la propiedad "DefaultFontName" en "Courier New" para,
  // mientras renderiza el documento, aplique esa fuente en todos los casos cuando otra fuente no esté disponible.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words ahora usará la fuente predeterminada en lugar de las fuentes faltantes durante cualquier llamada de procesamiento.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Ver también

* class [DefaultFontSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../defaultfontsubstitutionrule/)
* asamblea [Aspose.Words](../../../)


