---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
second_title: Aspose.Words for .NET API Reference
description: DocumentBase property. Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss in C#.
type: docs
weight: 90
url: /net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Remarks

Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [`PageCount`](../../document/pagecount/) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

## Examples

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

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Open a document that contains text formatted with a font that does not exist in any of our font sources.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Assign a callback for handling font substitution warnings.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Set a default font name and enable font substitution.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // We will get a font substitution warning if we save a document with a missing font.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // We can also verify warnings in the collection and clear them.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Called every time a warning occurs during loading/saving.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### See Also

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* namespace [Aspose.Words](../../documentbase/)
* assembly [Aspose.Words](../../../)
