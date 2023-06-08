---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words for .NET
description: FontSubstitutionSettings DefaultFontSubstitution property. Settings related to default font substitution rule in C#.
type: docs
weight: 10
url: /net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Settings related to default font substitution rule.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Examples

Shows how to set the default font substitution rule.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Get the default substitution rule within FontSettings.
// This rule will substitute all missing fonts with "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Set the default font substitute to "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// Using a document builder, add some text in a font that we do not have to see the substitution take place,
// and then render the result in a PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### See Also

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
