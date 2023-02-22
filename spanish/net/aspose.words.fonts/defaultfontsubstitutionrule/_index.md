---
title: Class DefaultFontSubstitutionRule
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule clase. Regla de sustitución de fuente predeterminada.
type: docs
weight: 2660
url: /es/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Regla de sustitución de fuente predeterminada.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Obtiene o establece el nombre de fuente predeterminado. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Especifica si la regla está habilitada o no. |

### Observaciones

Esta regla define un único nombre de fuente predeterminado que se utilizará para la sustitución si la fuente original no está disponible.

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

### Ver también

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


