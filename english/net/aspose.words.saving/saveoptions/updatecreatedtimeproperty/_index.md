---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words for .NET
description: SaveOptions UpdateCreatedTimeProperty property. Gets or sets a value determining whether the CreatedTime property is updated before saving. Default value is false in C#.
type: docs
weight: 150
url: /net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Gets or sets a value determining whether the [`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) property is updated before saving. Default value is `false`;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
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

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
