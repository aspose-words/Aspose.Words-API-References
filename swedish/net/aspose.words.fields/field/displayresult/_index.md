---
title: Field.DisplayResult
linktitle: DisplayResult
articleTitle: DisplayResult
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Field DisplayResult som levererar texten för dina visade fältresultat, vilket förbättrar tydligheten och användarupplevelsen.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/field/displayresult/
---
## Field.DisplayResult property

Hämtar texten som representerar det visade fältresultatet.

```csharp
public string DisplayResult { get; }
```

## Anmärkningar

Den[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) Metoden måste anropas för att få rätt värde för the [`FieldListNum`](../../fieldlistnum/) ,[`FieldAutoNum`](../../fieldautonum/) ,[`FieldAutoNumOut`](../../fieldautonumout/) och[`FieldAutoNumLgl`](../../fieldautonumlgl/) fält.

## Exempel

Visar hur man får den riktiga texten som ett fält visar i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This document was written by ");
FieldAuthor fieldAuthor = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
fieldAuthor.AuthorName = "John Doe";

// Vi kan använda DisplayResult-egenskapen för att verifiera exakt vilken text
// ett fält skulle visas på sin plats i dokumentet.
Assert.AreEqual(string.Empty, fieldAuthor.DisplayResult);

 // Fälten upprätthåller inte korrekta resultatvärden i realtid.
// För att säkerställa att våra fält visar korrekta resultat vid varje given tidpunkt,
// till exempel precis innan en sparoperation, måste vi uppdatera dem manuellt.
fieldAuthor.Update();

Assert.AreEqual("John Doe", fieldAuthor.DisplayResult);

doc.Save(ArtifactsDir + "Field.DisplayResult.docx");
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
