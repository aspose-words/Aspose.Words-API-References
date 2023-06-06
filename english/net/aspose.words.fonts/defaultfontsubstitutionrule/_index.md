---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule class. Default font substitution rule in C#.
type: docs
weight: 2810
url: /net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Default font substitution rule.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Properties

| Name | Description |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Gets or sets the default font name. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifies whether the rule is enabled or not. |

## Remarks

This rule defines single default font name to be used for substitution if the original font is not available.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
