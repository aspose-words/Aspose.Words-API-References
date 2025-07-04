---
title: WarningInfoCollection.Warning
linktitle: Warning
articleTitle: Warning
second_title: Aspose.Words for .NET
description: Discover the WarningInfoCollection method that enhances your application by implementing IWarningCallback, effortlessly adding warnings to your collection.
type: docs
weight: 60
url: /net/aspose.words/warninginfocollection/warning/
---
## WarningInfoCollection.Warning method

Implements the [`IWarningCallback`](../../iwarningcallback/) interface. Adds a warning to this collection.

```csharp
public void Warning(WarningInfo info)
```

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

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
