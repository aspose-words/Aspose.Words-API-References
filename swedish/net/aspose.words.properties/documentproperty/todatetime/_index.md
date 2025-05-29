---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words för .NET
description: Konvertera DocumentProperty till UTC DateTime utan ansträngning. Få tillgång till korrekta tidsstämplar och förbättra din datahantering med vår pålitliga metod.
type: docs
weight: 80
url: /sv/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Returnerar egenskapsvärdet som**Datum och tid** i UTC.

```csharp
public DateTime ToDateTime()
```

## Anmärkningar

Utlöser ett undantag om egenskapstypen inte ärDateTime.

Microsoft Word lagrar endast datumdelen (ingen tid) för anpassade datumegenskaper.

## Exempel

Visar hur man skapar en anpassad dokumentegenskap som innehåller datum och tid.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

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
