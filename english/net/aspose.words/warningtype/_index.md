---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WarningType enum, which categorizes warnings during document loading or saving, enhancing your document management experience.
type: docs
weight: 7540
url: /net/aspose.words/warningtype/
---
## WarningType enumeration

Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.

```csharp
[Flags]
public enum WarningType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DataLossCategory | `FF` | Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save. |
| DataLoss | `1` | Generic data loss, no specific code. |
| MajorFormattingLossCategory | `FF00` | The resulting document or a particular location in it might look substantially different compared to the original document. |
| MajorFormattingLoss | `100` | Generic major formatting loss, no specific code. |
| MinorFormattingLossCategory | `FF0000` | The resulting document or a particular location in it might look somewhat different compared to the original document. |
| MinorFormattingLoss | `10000` | Generic minor formatting loss, no specific code. |
| FontSubstitution | `20000` | Font has been substituted. |
| FontEmbedding | `40000` | Loss of embedded font information during document saving. |
| UnexpectedContentCategory | `F000000` | Some content in the source document could not be recognized (i.e. is unsupported), this may or may not cause issues or result in data/formatting loss. |
| UnexpectedContent | `1000000` | Generic unexpected content, no specific code. |
| Hint | `10000000` | Advises of a potential problem or suggests an improvement. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
