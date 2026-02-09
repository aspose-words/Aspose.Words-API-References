---
title: FontSubstitutionReason Enum
linktitle: FontSubstitutionReason
articleTitle: FontSubstitutionReason
second_title: Aspose.Words for .NET
description: Aspose.Words.FontSubstitutionReason enum shows the reason for font substitution to keep documents displayed correctly.
type: docs
weight: 3250
url: /net/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enumeration

Specifies the reason of font substitution.

```csharp
public enum FontSubstitutionReason
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AlternativeName | `0` | Font substitution by alternative name from the document. |
| FontNameSubstitutionRule | `1` | Font substitution by font name rule. |
| FontConfigSubstitutionRule | `2` | Font substitution by font config rule. |
| TableSubstitutionRule | `3` | Font substitution by table rule. |
| FontInfoSubstitutionRule | `4` | Font substitution by font info rule. |
| DefaultFontSubstitutionRule | `5` | Font substitution by default font rule. |
| FirstAvailableFont | `6` | Font substitution with the first available font. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
