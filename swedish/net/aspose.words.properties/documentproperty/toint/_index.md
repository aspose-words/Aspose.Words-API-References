---
title: DocumentProperty.ToInt
linktitle: ToInt
articleTitle: ToInt
second_title: Aspose.Words för .NET
description: Konvertera DocumentProperty-värden till heltal utan ansträngning med ToInt-metoden. Lås upp sömlös datahantering för dina applikationer!
type: docs
weight: 100
url: /sv/net/aspose.words.properties/documentproperty/toint/
---
## DocumentProperty.ToInt method

Returnerar egenskapsvärdet som ett heltal.

```csharp
public int ToInt()
```

## Anmärkningar

Utlöser ett undantag om egenskapstypen inte ärNumber .

## Exempel

Visar olika typkonverteringsmetoder för anpassade dokumentegenskaper.

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

### Se även

* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
