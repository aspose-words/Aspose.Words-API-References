---
title: DocumentProperty.ToInt
linktitle: ToInt
articleTitle: ToInt
second_title: Aspose.Words for .NET
description: Convert DocumentProperty values to integers effortlessly with the ToInt method. Unlock seamless data handling for your applications!
type: docs
weight: 100
url: /net/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty.ToInt method

Returns the property value as integer.

```csharp
public int ToInt()
```

## Remarks

Throws an exception if the property type is not Number.

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

### See Also

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
