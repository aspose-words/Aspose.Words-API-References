---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.WarningInfoCollection, a powerful class for managing WarningInfo objects, enhancing document processing and error handling.
type: docs
weight: 7580
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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
