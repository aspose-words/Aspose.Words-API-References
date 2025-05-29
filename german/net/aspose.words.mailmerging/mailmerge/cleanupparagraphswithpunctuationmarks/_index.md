---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Serienbrief mit der Eigenschaft „CleanupParagraphsWithPunctuationMarks“. Kontrollieren Sie die Entfernung leerer Absätze für sauberere, professionelle Dokumente.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Ruft einen Wert ab oder legt ihn fest, der angibt, ob Absätze mit Satzzeichen als leer betrachtet werden und entfernt werden sollen, wenn dieRemoveEmptyParagraphs Option angegeben ist.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

Hier ist die vollständige Liste der löschbaren Satzzeichen:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

## Beispiele

Zeigt, wie Absätze mit Satzzeichen nach einem Seriendruckvorgang entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Konfigurieren Sie die Eigenschaft „CleanupOptions“, um alle leeren Absätze zu entfernen, die durch diesen Seriendruck entstehen würden.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Wenn Sie die Eigenschaft „CleanupParagraphsWithPunctuationMarks“ auf „true“ setzen, werden auch Absätze gezählt
// mit Satzzeichen als leer und wird durch die Serienbriefoperation dazu gebracht, diese ebenfalls zu entfernen.
// Setzen der Eigenschaft „CleanupParagraphsWithPunctuationMarks“ auf „false“
// entfernt leere Absätze, aber keine mit Satzzeichen.
// Dies ist eine Liste von Satzzeichen, die diese Eigenschaft betrifft: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
