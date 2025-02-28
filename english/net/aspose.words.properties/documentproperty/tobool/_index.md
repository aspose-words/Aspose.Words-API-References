---
title: DocumentProperty.ToBool
linktitle: ToBool
articleTitle: ToBool
second_title: Aspose.Words for .NET
description: Discover the DocumentProperty ToBool method that efficiently converts property values to boolean for seamless data handling and enhanced coding efficiency.
type: docs
weight: 60
url: /net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

Returns the property value as bool.

```csharp
public bool ToBool()
```

## Remarks

Throws an exception if the property type is not Boolean.

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

Assert.AreEqual(true, properties["Authorized"].ToBool());
Assert.AreEqual("John Doe", properties["Authorized By"].ToString());
Assert.AreEqual(authDate, properties["Authorized Date"].ToDateTime());
Assert.AreEqual(1, properties["Authorized Revision"].ToInt());
Assert.AreEqual(123.45d, properties["Authorized Amount"].ToDouble());
```

### See Also

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
