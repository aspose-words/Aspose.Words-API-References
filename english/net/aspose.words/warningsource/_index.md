---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WarningSource enum, identifying warning sources during document loading and saving for enhanced document management.
type: docs
weight: 7560
url: /net/aspose.words/warningsource/
---
## WarningSource enumeration

Specifies the module that produces a warning during document loading or saving.

```csharp
public enum WarningSource
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | `0` | The warning source is not specified. |
| Layout | `1` | Module that builds a document layout. |
| DrawingML | `2` | Module that renders DrawingML shapes. |
| OfficeMath | `3` | Module that renders OfficeMath. |
| Shapes | `4` | Module that renders ordinary shapes. |
| Metafile | `5` | Module that renders metafiles. |
| Xps | `6` | Module that renders XPS. |
| Pdf | `7` | Module that renders PDF. |
| Image | `8` | Module that renders images. |
| Docx | `9` | Module that reads/writes DOCX files. |
| Doc | `10` | Module that reads/writes binary DOC files. |
| Text | `11` | Module that reads/writes plaintext files. |
| Rtf | `12` | Module that reads/writes RTF files. |
| WordML | `13` | Module that reads/writes WML files. |
| Nrx | `14` | Common modules that are shared between DOCX/WML reader/writer modules. |
| Odt | `15` | Module that reads/writes ODT files. |
| Html | `16` | Module that reads/writes HTML/MHTML files. |
| Validator | `17` | Module that verifies model consistency and validity. |
| Xaml | `18` | Module that reads/writes Xaml files. |
| Svm | `19` | Module that reads Svm files. |
| MathML | `20` | Module that reads W3C MathML files. |
| Font | `21` | Module that reads font files. |
| Svg | `22` | Module that reads SVG files. |
| Markdown | `23` | Module that reads/writes Markdown files. |
| Chm | `24` | Module that reads CHM files. |
| Epub | `25` | Module that reads/writes EPUB files. |
| Xml | `26` | Module that reads XML files. |
| Xlsx | `27` | Module that writes XLSX files. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
