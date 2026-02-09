---
title: FontInfoSubstitutionRule Class
linktitle: FontInfoSubstitutionRule
articleTitle: FontInfoSubstitutionRule
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fonts.FontInfoSubstitutionRule class to optimize font management in your documents with seamless substitution capabilities.
type: docs
weight: 3390
url: /net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Font info substitution rule.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Properties

| Name | Description |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Specifies whether the rule is enabled or not. |

## Remarks

According to this rule Aspose.Words evaluates all the related fields in [`FontInfo`](../fontinfo/) (Panose, Sig etc) for the missing font and finds the closest match among the available font sources. If [`FontInfo`](../fontinfo/) is not available for the missing font then nothing will be done.

## Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```csharp
// Open a document that contains text formatted with a font that does not exist in any of our font sources.
Document doc = new Document(MyDir + "Missing font.docx");

// Assign a callback for handling font substitution warnings.
WarningInfoCollection warningCollector = new WarningInfoCollection();
doc.WarningCallback = warningCollector;

// Set a default font name and enable font substitution.
FontSettings fontSettings = new FontSettings();
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

// Original font metrics should be used after font substitution.
doc.LayoutOptions.KeepOriginalFontMetrics = true;

// We will get a font substitution warning if we save a document with a missing font.
doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

foreach (WarningInfo info in warningCollector)
{
    if (info.WarningType == WarningType.FontSubstitution)
        Console.WriteLine(info.Description);
}
```

### See Also

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
