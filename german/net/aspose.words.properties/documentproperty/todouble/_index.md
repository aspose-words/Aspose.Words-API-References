---
title: DocumentProperty.ToDouble
linktitle: ToDouble
articleTitle: ToDouble
second_title: Aspose.Words für .NET
description: DocumentProperty ToDouble methode. Gibt den Eigenschaftswert als double. zurück in C#.
type: docs
weight: 90
url: /de/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Gibt den Eigenschaftswert als double. zurück.

```csharp
public double ToDouble()
```

## Bemerkungen

Löst eine Ausnahme aus, wenn der Eigenschaftstyp nicht vorhanden istNumber .

## Beispiele

Zeigt verschiedene Typkonvertierungsmethoden für benutzerdefinierte Dokumenteigenschaften.

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

### Siehe auch

* class [DocumentProperty](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
