---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.PropertyType enum to easily define document property data types for enhanced document management and customization.
type: docs
weight: 5280
url: /net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Specifies data type of a document property.

```csharp
public enum PropertyType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Boolean | `0` | The property is a boolean value. |
| DateTime | `1` | The property is a date time value. |
| Double | `2` | The property is a floating number. |
| Number | `3` | The property is an integer number. |
| String | `4` | The property is a string value. |
| StringArray | `5` | The property is an array of strings. |
| ObjectArray | `6` | The property is an array of objects. |
| ByteArray | `7` | The property is an array of bytes. |
| Other | `8` | The property is some other type. |

## Examples

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.That(properties.Count, Is.EqualTo(0));

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.That(properties.IndexOf("Authorized Amount"), Is.EqualTo(1));
Assert.That(properties.Count, Is.EqualTo(5));

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

Assert.That(field.Result, Is.EqualTo("John Doe"));

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.That(properties.Contains("Authorized Amount"), Is.False);
Assert.That(properties.Count, Is.EqualTo(4));

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.That(properties.Contains("Authorized Revision"), Is.False);
Assert.That(properties.Count, Is.EqualTo(3));

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* namespace [Aspose.Words.Properties](../../aspose.words.properties/)
* assembly [Aspose.Words](../../)
