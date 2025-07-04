---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words for .NET
description: Convert DocumentProperty to UTC DateTime effortlessly. Access accurate timestamps and enhance your data management with our reliable method.
type: docs
weight: 80
url: /net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Returns the property value as **DateTime** in UTC.

```csharp
public DateTime ToDateTime()
```

## Remarks

Throws an exception if the property type is not DateTime.

Microsoft Word stores only the date part (no time) for custom date properties.

## Examples

Shows how to create a custom document property which contains a date and time.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

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
