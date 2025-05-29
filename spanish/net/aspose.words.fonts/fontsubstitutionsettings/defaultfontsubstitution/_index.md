---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad DefaultFontSubstitution optimiza la configuración de fuentes para una tipografía impecable. Mejore su diseño con reglas de sustitución de fuentes eficaces.
type: docs
weight: 10
url: /es/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Configuraciones relacionadas con la regla de sustitución de fuente predeterminada.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Ejemplos

Muestra cómo establecer la regla de sustitución de fuente predeterminada.

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

// Establezca la fuente sustituta predeterminada en "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Usando un generador de documentos, agregue algo de texto en una fuente que no tengamos que ver cuando se realice la sustitución.
// y luego renderizar el resultado en formato PDF.
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
