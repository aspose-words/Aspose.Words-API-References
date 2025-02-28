---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: Aspose.Words for .NET
description: Discover the BuiltInDocumentProperties LastPrinted feature to easily track your document's last print date in UTC. Enhance your workflow today!
type: docs
weight: 160
url: /net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

Gets or sets the date when the document was last printed in UTC.

```csharp
public DateTime LastPrinted { get; set; }
```

## Remarks

For documents originated from RTF format this property returns the local time of last print operation.

If the document was never printed, this property will return DateTime.MinValue.

Aspose.Words does not update this property.

## Examples

Shows how to work with document properties in the "Origin" category.

```csharp
// Open a document that we have created and edited using Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// The following built-in properties contain information regarding the creation and editing of this document.
// We can right-click this document in Windows Explorer and find
// these properties via "Properties" -> "Details" -> "Origin" category.
// Fields such as PRINTDATE and EDITTIME can display these values in the document body.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// We can also change the values of built-in properties.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word updates the following properties automatically when we save the document.
// To use these properties with Aspose.Words, we will need to set values for them manually.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
