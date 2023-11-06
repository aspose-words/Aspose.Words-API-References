---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.WarningInfoCollection class. Represents a typed collection of WarningInfo objects in C#.
type: docs
weight: 6660
url: /net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Represents a typed collection of [`WarningInfo`](../warninginfo/) objects.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Constructors

| Name | Description |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Gets an item at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Removes all elements from the collection. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implements the [`IWarningCallback`](../iwarningcallback/) interface. Adds a warning to this collection. |

## Remarks

You can use this collection object as the simplest form of [`IWarningCallback`](../iwarningcallback/) implementation to gather all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it to the [`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) or [`WarningCallback`](../documentbase/warningcallback/) property.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
