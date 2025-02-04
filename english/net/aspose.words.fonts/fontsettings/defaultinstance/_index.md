---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words for .NET
description: FontSettings DefaultInstance property. Static default font settings in C#.
type: docs
weight: 20
url: /net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Static default font settings.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Remarks

This instance is used by default in a document unless [`FontSettings`](../../../aspose.words/document/fontsettings/) is specified.

## Examples

Shows how to configure the default font settings instance.

```csharp
// Configure the default font settings instance to use the "Courier New" font
// as a backup substitute when we attempt to use an unknown font.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// This document does not have a FontSettings configuration. When we render the document,
// the default FontSettings instance will resolve the missing font.
// Aspose.Words will use "Courier New" to render text that uses the unknown font.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Store the current collection of font sources, which will be the default font source for every document
    // for which we do not specify a different font source.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // When rendering the document, there will be no place to find the "Times New Roman" font.
    // This will cause a font substitution warning, which our callback will detect.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Called every time a warning occurs during loading/saving.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### See Also

* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
