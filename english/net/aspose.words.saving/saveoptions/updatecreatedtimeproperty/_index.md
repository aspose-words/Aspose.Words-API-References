---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words for .NET
description: Optimize your SaveOptions with the UpdateCreatedTimeProperty. Control CreatedTime updates before saving, enhancing data accuracy. Default, false.
type: docs
weight: 160
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

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// This flag determines whether the created time, which is a built-in property, is updated.
// If so, then the date of the document's most recent save operation
// with this SaveOptions object passed as a parameter is used as the created time.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Open the saved document, then verify the value of the property.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.That(doc.BuiltInDocumentProperties.CreatedTime, Is.Not.EqualTo(createdTime));
else
    Assert.That(doc.BuiltInDocumentProperties.CreatedTime, Is.EqualTo(createdTime));
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
