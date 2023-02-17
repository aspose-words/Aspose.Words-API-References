---
title: SaveOptions.UpdateLastPrintedProperty
second_title: Aspose.Words for .NET API Reference
description: SaveOptions property. Gets or sets a value determining whether the LastPrinted property is updated before saving in C#.
type: docs
weight: 170
url: /net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Gets or sets a value determining whether the [`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) property is updated before saving.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Examples

Shows how to update a document's "CreatedTime" property when saving.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// This flag determines whether the created time, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the created time.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Open the saved document, then verify the value of the property.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

Shows how to update a document's "Last printed" property when saving.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

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

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../saveoptions/)
* assembly [Aspose.Words](../../../)
