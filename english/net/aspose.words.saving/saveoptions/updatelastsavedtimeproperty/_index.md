---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words for .NET
description: Optimize your SaveOptions with the UpdateLastSavedTimeProperty. Control LastSavedTime updates for efficient data management and enhanced performance.
type: docs
weight: 180
url: /net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Gets or sets a value determining whether the [`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) property is updated before saving.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Examples

Shows how to determine whether to preserve the document's "Last saved time" property when saving.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "UpdateLastSavedTimeProperty" property to "true" to
// set the output document's "Last saved time" built-in property to the current date/time.
// Set the "UpdateLastSavedTimeProperty" property to "false" to
// preserve the original value of the input document's "Last saved time" built-in property.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### See Also

* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
