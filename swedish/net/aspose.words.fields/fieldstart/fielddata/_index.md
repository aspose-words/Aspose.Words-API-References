---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words för .NET
description: FieldStart FieldData fast egendom. Hämtar anpassade fältdata som är associerade med fältet i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Hämtar anpassade fältdata som är associerade med fältet.

```csharp
public byte[] FieldData { get; }
```

## Exempel

Visar hur man får data kopplade till fältet.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Se även

* class [FieldStart](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
