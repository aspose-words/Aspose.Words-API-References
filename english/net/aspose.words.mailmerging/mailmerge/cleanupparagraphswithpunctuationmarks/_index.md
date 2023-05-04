---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words for .NET
description: MailMerge CleanupParagraphsWithPunctuationMarks property. Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the RemoveEmptyParagraphs option is specified in C#.
type: docs
weight: 20
url: /net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Gets or sets a value indicating whether paragraphs with punctuation marks are considered as empty and should be removed if the RemoveEmptyParagraphs option is specified.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Remarks

The default value is `true`.

Here is the complete list of cleanable punctuation marks:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

## Examples

Shows how to remove paragraphs with punctuation marks after a mail merge operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Configure the "CleanupOptions" property to remove any empty paragraphs that this mail merge would create.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Setting the "CleanupParagraphsWithPunctuationMarks" property to "true" will also count paragraphs
// with punctuation marks as empty and will get the mail merge operation to remove them as well.
// Setting the "CleanupParagraphsWithPunctuationMarks" property to "false"
// will remove empty paragraphs, but not ones with punctuation marks.
// This is a list of punctuation marks that this property concerns: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### See Also

* class [MailMerge](../)
* namespace [Aspose.Words.MailMerging](../../mailmerge/)
* assembly [Aspose.Words](../../../)
