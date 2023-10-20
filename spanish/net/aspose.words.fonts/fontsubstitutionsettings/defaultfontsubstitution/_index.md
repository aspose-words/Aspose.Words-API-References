---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words para .NET
description: FontSubstitutionSettings DefaultFontSubstitution propiedad. Configuraciones relacionadas con la regla de sustitución de fuentes predeterminada en C#.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Configuraciones relacionadas con la regla de sustitución de fuentes predeterminada.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Ejemplos

Muestra cómo configurar la regla de sustitución de fuentes predeterminada.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Obtenga la regla de sustitución predeterminada dentro de FontSettings.
// Esta regla sustituirá todas las fuentes que falten por "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Establece el sustituto de fuente predeterminado en "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Utilizando un generador de documentos, agrega texto en una fuente que no tengamos que ver cómo se realiza la sustitución,
// y luego renderizar el resultado en un PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Ver también

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
