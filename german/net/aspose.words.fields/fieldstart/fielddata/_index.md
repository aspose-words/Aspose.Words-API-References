---
title: FieldStart.FieldData
linktitle: FieldData
articleTitle: FieldData
second_title: Aspose.Words für .NET
description: Schalten Sie benutzerdefinierte Felddaten mit der FieldData-Eigenschaft von FieldStart frei, verbessern Sie Ihr Datenmanagement und steigern Sie mühelos die Produktivität.
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldstart/fielddata/
---
## FieldStart.FieldData property

Ruft benutzerdefinierte Felddaten ab, die mit dem Feld verknüpft sind.

```csharp
public byte[] FieldData { get; }
```

## Beispiele

Zeigt, wie die mit dem Feld verknüpften Daten abgerufen werden.

```csharp
Document doc = new Document(MyDir + "Field sample - Field with data.docx");

Field field = doc.Range.Fields[2];
Console.WriteLine(Encoding.UTF8.GetString(field.Start.FieldData));
```

### Siehe auch

* class [FieldStart](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
