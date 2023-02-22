---
title: Field.DisplayResult
second_title: Aspose.Words för .NET API Referens
description: Field fast egendom. Hämtar texten som representerar det visade fältresultatet.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Hämtar texten som representerar det visade fältresultatet.

```csharp
public string DisplayResult { get; }
```

### Anmärkningar

Den[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) metod måste anropas för att erhålla korrekt värde för [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) och[`FieldAutoNumLgl`](../../fieldautonumlgl/) fields.

### Exempel

Visar hur man får fram den verkliga texten som ett fält visar i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Vi kan använda egenskapen DisplayResult för att verifiera vilken exakt text
// ett fält skulle visas på dess plats i dokumentet.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

  // Fält upprätthåller inte korrekta resultatvärden i realtid.
// För att säkerställa att våra fält visar korrekta resultat vid varje given tidpunkt,
// som precis innan en lagringsoperation måste vi uppdatera dem manuellt.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../field/)
* hopsättning [Aspose.Words](../../../)


