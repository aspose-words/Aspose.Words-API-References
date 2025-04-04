---
title: WarningInfo Class
linktitle: WarningInfo
articleTitle: WarningInfo
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WarningInfo class, which provides crucial insights into warnings during document loading or saving, enhancing your workflow efficiency.
type: docs
weight: 7460
url: /net/aspose.words/warninginfo/
---
## WarningInfo class

Contains information about a warning that Aspose.Words issued during document loading or saving.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class WarningInfo
```

## Properties

| Name | Description |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Returns the description of the warning. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Returns the source of the warning. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Returns the type of the warning. |

## Remarks

You do not create instances of this class. Objects of this class are created and passed by Aspose.Words to the [`Warning`](../iwarningcallback/warning/) method.

## Examples

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```csharp
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

    // Original font metrics should be used after font substitution.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

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

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
