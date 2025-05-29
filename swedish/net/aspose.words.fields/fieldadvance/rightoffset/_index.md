---
title: FieldAdvance.RightOffset
linktitle: RightOffset
articleTitle: RightOffset
second_title: Aspose.Words för .NET
description: Upptäck FieldAdvance RightOffset-egenskapen, justera enkelt textpositionering med exakt punktkontroll för förbättrad dokumentformatering och tydlighet.
type: docs
weight: 50
url: /sv/net/aspose.words.fields/fieldadvance/rightoffset/
---
## FieldAdvance.RightOffset property

Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas åt höger med.

```csharp
public string RightOffset { get; set; }
```

## Exempel

Visar hur man infogar ett ADVANCE-fält och redigerar dess egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Nedan följer två sätt att använda fältet ADVANCE för att justera positionen för text som följer det.
// Effekterna av ett ADVANCE-fält fortsätter att tillämpas tills stycket slutar,
// eller ett annat ADVANCE-fält uppdaterar offset-/koordinatvärdena.
// 1 - Ange en riktningsförskjutning:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Flytta text till en position som anges med koordinater:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Se även

* class [FieldAdvance](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
