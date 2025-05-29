---
title: DocumentProperty.ToDouble
linktitle: ToDouble
articleTitle: ToDouble
second_title: Aspose.Words für .NET
description: Konvertieren Sie DocumentProperty-Werte mühelos in Double mit der ToDouble-Methode. Profitieren Sie noch heute von präziser Datenverarbeitung für Ihre Anwendungen!
type: docs
weight: 90
url: /de/net/aspose.words.properties/documentproperty/todouble/
---
## DocumentProperty.ToDouble method

Gibt den Eigenschaftswert als Double zurück.

```csharp
public double ToDouble()
```

## Bemerkungen

Löst eine Exception aus, wenn der Eigenschaftstyp nichtNumber .

## Beispiele

Zeigt verschiedene Methoden zur Typkonvertierung benutzerdefinierter Dokumenteigenschaften.

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
