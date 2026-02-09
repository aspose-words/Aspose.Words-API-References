---
title: FontSubstitutionWarningInfo Class
linktitle: FontSubstitutionWarningInfo
articleTitle: FontSubstitutionWarningInfo
second_title: Aspose.Words for .NET
description: Aspose.Words.FontSubstitutionWarningInfo class provides details on font substitution warnings during document load or save.
type: docs
weight: 3260
url: /net/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class

Contains information about a font substitution warning that Aspose.Words issued during document loading or saving.

```csharp
public class FontSubstitutionWarningInfo : WarningInfo
```

## Properties

| Name | Description |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Returns the description of the warning. |
| [Reason](../../aspose.words/fontsubstitutionwarninginfo/reason/) { get; } | Font substitution reason. |
| [RequestedBold](../../aspose.words/fontsubstitutionwarninginfo/requestedbold/) { get; } | Indicates whether bold style was requested. |
| [RequestedFamilyName](../../aspose.words/fontsubstitutionwarninginfo/requestedfamilyname/) { get; } | Requested font family name. |
| [RequestedItalic](../../aspose.words/fontsubstitutionwarninginfo/requesteditalic/) { get; } | Indicates whether italic style was requested. |
| [ResolvedFont](../../aspose.words/fontsubstitutionwarninginfo/resolvedfont/) { get; } | Resolved font. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Returns the source of the warning. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Returns the type of the warning. |

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

* class [WarningInfo](../warninginfo/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
