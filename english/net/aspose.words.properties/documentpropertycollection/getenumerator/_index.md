---
title: DocumentPropertyCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words for .NET
description: Discover the DocumentPropertyCollection GetEnumerator method. Easily iterate through all collection items with this efficient enumerator for seamless data access.
type: docs
weight: 50
url: /net/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection.GetEnumerator method

Returns an enumerator object that can be used to iterate over all items in the collection.

```csharp
public IEnumerator<DocumentProperty> GetEnumerator()
```

## Examples

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Print every custom property in the document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Display the value of a custom property using a DOCPROPERTY field.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
