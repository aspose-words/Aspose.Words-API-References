---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words für .NET
description: FieldStart FieldData eigendom. Ruft benutzerdefinierte Felddaten ab die dem Feld zugeordnet sind in C#.
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Ruft benutzerdefinierte Felddaten ab, die dem Feld zugeordnet sind.

```csharp
public byte[] FieldData { get; }
```

## Beispiele

Zeigt, wie mit dem Feld verknüpfte Daten abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.Default.GetString(field.Start.FieldData));
```

### Siehe auch

* class [FieldStart](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
