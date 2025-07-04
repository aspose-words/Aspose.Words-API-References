---
title: DocumentProperty.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words for .NET
description: Discover the DocumentProperty ToString method, which formats property values as strings based on locale, enhancing data presentation and user experience.
type: docs
weight: 110
url: /net/aspose.words.properties/documentproperty/tostring/
---
## DocumentProperty.ToString method

Returns the property value as a string formatted according to the current locale.

```csharp
public override string ToString()
```

## Remarks

Converts a boolean property into "Y" or "N". Converts a date property into a short date string. For all other types converts a property using Object.ToString().

## Examples

Shows various type conversion methods of custom document properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

DateTime authDate = DateTime.Today;
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", authDate);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

Assert.That(properties["Authorized"].ToBool(), Is.EqualTo(true));
Assert.That(properties["Authorized By"].ToString(), Is.EqualTo("John Doe"));
Assert.That(properties["Authorized Date"].ToDateTime(), Is.EqualTo(authDate));
Assert.That(properties["Authorized Revision"].ToInt(), Is.EqualTo(1));
Assert.That(properties["Authorized Amount"].ToDouble(), Is.EqualTo(123.45d));
```

Shows how to work with custom document properties.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties. 
Assert.That(doc.CustomDocumentProperties["CustomProperty"].ToString(), Is.EqualTo("Value of custom document property"));

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### See Also

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
