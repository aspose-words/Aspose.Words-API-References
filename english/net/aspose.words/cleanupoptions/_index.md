---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.CleanupOptions to customize document cleaning. Enhance your workflow with tailored settings for cleaner, more efficient documents.
type: docs
weight: 400
url: /net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Allows to specify options for document cleaning.

To learn more, visit the [Clean Up a Document](https://docs.aspose.com/words/net/clean-up-a-document/) documentation article.

```csharp
public class CleanupOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Gets/sets a flag indicating whether duplicate styles should be removed from document. Default value is `false`. |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Specifies that unused [`BuiltIn`](../style/builtin/) styles should be removed from document. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Specifies whether unused list and list definitions should be removed from document. Default value is `true`. |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Specifies whether unused styles should be removed from document. Default value is `true`. |

## Examples

Shows how to remove all unused custom styles from a document.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combined with the built-in styles, the document now has eight styles.
// A custom style is marked as "used" while there is any text within the document
// formatted in that style. This means that the 4 styles we added are currently unused.
Assert.AreEqual(8, doc.Styles.Count);

// Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Now, there is one unused character style and one unused list style.
// The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

// Removing every node that a custom style is applied to marks it as "unused" again. 
// Rerun the Cleanup method to remove them.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
