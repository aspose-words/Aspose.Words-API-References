---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words for .NET
description: Discover the WarningInfo Source property that reveals the origin of warnings, enhancing your application's reliability and user experience.
type: docs
weight: 20
url: /net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Returns the source of the warning.

```csharp
public WarningSource Source { get; }
```

## Examples

Shows how to work with the warning source.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.That(warningInfo.Description, Is.EqualTo("The (*, 0:11) cannot be properly written into Markdown."));
}
```

Shows how to get additional information about font substitution.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

WarningInfoCollection callback = new WarningInfoCollection();
doc.WarningCallback = callback;

FontSettings fontSettings = new FontSettings();
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Arial", "Arvo", "Slab");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarnings.pdf");

FontSubstitutionWarningInfo warningInfo = (FontSubstitutionWarningInfo)callback[0];
Assert.That(warningInfo.Source, Is.EqualTo(WarningSource.Layout));
Assert.That(warningInfo.WarningType, Is.EqualTo(WarningType.FontSubstitution));
Assert.That(warningInfo.Reason, Is.EqualTo(FontSubstitutionReason.TableSubstitutionRule));
Assert.That(warningInfo.Description, Is.EqualTo("Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution."));
Assert.That(warningInfo.RequestedBold, Is.True);
Assert.That(warningInfo.RequestedItalic, Is.False);
Assert.That(warningInfo.RequestedFamilyName, Is.EqualTo("Arial"));
```

### See Also

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
