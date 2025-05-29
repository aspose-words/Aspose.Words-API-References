---
title: DocumentProperty.ToBool
linktitle: ToBool
articleTitle: ToBool
second_title: Aspose.Words för .NET
description: Upptäck DocumentProperty ToBool-metoden som effektivt konverterar egenskapsvärden till booleska värden för sömlös datahantering och förbättrad kodningseffektivitet.
type: docs
weight: 60
url: /sv/net/aspose.words.properties/documentproperty/tobool/
---
## DocumentProperty.ToBool method

Returnerar egenskapsvärdet som bool.

```csharp
public bool ToBool()
```

## Anmärkningar

Utlöser ett undantag om egenskapstypen inte ärBoolean.

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
