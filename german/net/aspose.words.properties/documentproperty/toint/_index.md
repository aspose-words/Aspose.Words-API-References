---
title: DocumentProperty.ToInt
linktitle: ToInt
articleTitle: ToInt
second_title: Aspose.Words für .NET
description: Konvertieren Sie DocumentProperty-Werte mühelos in Ganzzahlen mit der ToInt-Methode. Ermöglichen Sie nahtloses Datenhandling für Ihre Anwendungen!
type: docs
weight: 100
url: /de/net/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty.ToInt method

Gibt den Eigenschaftswert als Ganzzahl zurück.

```csharp
public int ToInt()
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
