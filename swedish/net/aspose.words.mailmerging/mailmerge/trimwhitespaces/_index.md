---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words för .NET
description: Optimera din dokumentkopplingsprocess med egenskapen TrimWhitespaces, vilket säkerställer rena data genom att ta bort inledande och efterföljande mellanslag för korrekta resultat.
type: docs
weight: 130
url: /sv/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Hämtar eller anger ett värde som anger om efterföljande och inledande blanksteg ska tas bort från värden för koppling av dokument.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` .

## Exempel

Visar hur man tar bort blanksteg från värden i en datakälla när man kör en dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
