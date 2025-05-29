---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.DefaultFontSubstitutionRule para una gestión fluida de fuentes y un formato de documentos mejorado. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 3250
url: /es/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Regla de sustitución de fuente predeterminada.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Obtiene o establece el nombre de fuente predeterminado. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Especifica si la regla está habilitada o no. |

## Observaciones

Esta regla define un único nombre de fuente predeterminado que se utilizará para la sustitución si la fuente original no está disponible.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
