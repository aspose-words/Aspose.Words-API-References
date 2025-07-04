---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words for .NET
description: Optimize document management with SaveOptions UpdateLastPrintedProperty. Control LastPrinted updates for efficient saving and enhanced workflow.
type: docs
weight: 180
url: /net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Gets or sets a value determining whether the [`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Examples

Shows how to update a document's "Last printed" property when saving.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// This flag determines whether the last printed date, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the print date.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// In Microsoft Word 2003, this property can be found via File -> Properties -> Statistics -> Printed.
// It can also be displayed in the document's body by using a PRINTDATE field.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Open the saved document, then verify the value of the property.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.That(doc.BuiltInDocumentProperties.LastPrinted, Is.Not.EqualTo(lastPrinted));
else
    Assert.That(doc.BuiltInDocumentProperties.LastPrinted, Is.EqualTo(lastPrinted));
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
