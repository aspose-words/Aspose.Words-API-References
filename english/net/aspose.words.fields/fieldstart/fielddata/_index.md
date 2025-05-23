---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words for .NET
description: Unlock custom field data with FieldStart's FieldData property, enhancing your data management and boosting productivity effortlessly.
type: docs
weight: 10
url: /net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Gets custom field data which is associated with the field.

```csharp
public byte[] FieldData { get; }
```

## Examples

Shows how to get data associated with the field.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### See Also

* class [FieldStart](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
