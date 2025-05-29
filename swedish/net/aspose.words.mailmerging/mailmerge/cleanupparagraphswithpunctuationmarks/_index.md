---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words för .NET
description: Optimera din MailMerge med egenskapen CleanupParagraphsWithPunctuationMarks. Kontrollera borttagning av tomma stycken för renare, professionellare dokument.
type: docs
weight: 20
url: /sv/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Hämtar eller anger ett värde som anger om stycken med skiljetecken ska betraktas som tomma och ska tas bort omRemoveEmptyParagraphs alternativet är angivet.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Anmärkningar

Standardvärdet är`sann` .

Här är den kompletta listan över rensbara skiljetecken:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

## Exempel

Visar hur man tar bort stycken med skiljetecken efter en dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Konfigurera egenskapen "CleanupOptions" för att ta bort alla tomma stycken som den här dokumentkopplingen skulle skapa.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Om egenskapen "CleanupParagraphsWithPunctuationMarks" sätts till "true" räknas även stycken
// med skiljetecken som tomma och kommer att få dokumentkopplingsoperationen att ta bort dem också.
// Ställer in egenskapen "CleanupParagraphsWithPunctuationMarks" till "false"
// tar bort tomma stycken, men inte de med skiljetecken.
// Detta är en lista över skiljetecken som den här egenskapen berör: "!", "", "", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
