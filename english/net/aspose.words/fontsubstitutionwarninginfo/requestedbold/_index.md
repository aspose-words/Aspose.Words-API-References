---
title: FontSubstitutionWarningInfo.RequestedBold
linktitle: RequestedBold
articleTitle: RequestedBold
second_title: Aspose.Words for .NET
description: FontSubstitutionWarningInfo.RequestedBold property indicates if bold font style was requested in Aspose.Words.
type: docs
weight: 20
url: /net/aspose.words/fontsubstitutionwarninginfo/requestedbold/
---
## FontSubstitutionWarningInfo.RequestedBold property

Indicates whether bold style was requested.

```csharp
public bool RequestedBold { get; }
```

## Examples

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

* class [FontSubstitutionWarningInfo](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
