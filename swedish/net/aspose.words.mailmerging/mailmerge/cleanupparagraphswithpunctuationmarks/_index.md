---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words för .NET
description: MailMerge CleanupParagraphsWithPunctuationMarks fast egendom. Hämtar eller ställer in ett värde som anger om stycken med skiljetecken anses vara tomma och bör tas bort omRemoveEmptyParagraphs alternativet är specificerat i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Hämtar eller ställer in ett värde som anger om stycken med skiljetecken anses vara tomma och bör tas bort omRemoveEmptyParagraphs alternativet är specificerat.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Anmärkningar

Standardvärdet är`Sann` .

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

Visar hur man tar bort stycken med skiljetecken efter en kopplingsoperation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Konfigurera "CleanupOptions"-egenskapen för att ta bort alla tomma stycken som den här sammanslagningen skulle skapa.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Om du ställer in egenskapen "CleanupParagraphsWithPunctuationMarks" till "true" räknas också stycken
// med skiljetecken som tomma och kommer att få kopplingsoperationen för att ta bort dem också.
// Ställ in egenskapen "CleanupParagraphsWithPunctuationMarks" till "false"
// tar bort tomma stycken, men inte de med skiljetecken.
// Detta är en lista över skiljetecken som den här egenskapen gäller: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
