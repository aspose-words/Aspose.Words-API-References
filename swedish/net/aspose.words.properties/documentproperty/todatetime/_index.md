---
title: DocumentProperty.ToDateTime
linktitle: ToDateTime
articleTitle: ToDateTime
second_title: Aspose.Words för .NET
description: DocumentProperty ToDateTime metod. Returnerar egenskapsvärdet somDatum Tid i UTC i C#.
type: docs
weight: 80
url: /sv/net/aspose.words.properties/documentproperty/todatetime/
---
## DocumentProperty.ToDateTime method

Returnerar egenskapsvärdet som**Datum Tid** i UTC.

```csharp
public DateTime ToDateTime()
```

## Anmärkningar

Kastar ett undantag om egenskapstypen inte är detDateTime.

Microsoft Word lagrar endast datumdelen (ingen tid) för anpassade datumegenskaper.

## Exempel

Visar hur man skapar en anpassad dokumentegenskap som innehåller ett datum och en tid.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

Visar olika typer av konverteringsmetoder för anpassade dokumentegenskaper.

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
