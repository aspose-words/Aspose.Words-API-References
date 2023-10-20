---
title: MailMerge.CleanupParagraphsWithPunctuationMarks
linktitle: CleanupParagraphsWithPunctuationMarks
articleTitle: CleanupParagraphsWithPunctuationMarks
second_title: Aspose.Words для .NET
description: MailMerge CleanupParagraphsWithPunctuationMarks свойство. Получает или задает значение указывающее считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены еслиRemoveEmptyParagraphs указана опция на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/
---
## MailMerge.CleanupParagraphsWithPunctuationMarks property

Получает или задает значение, указывающее, считаются ли абзацы со знаками препинания пустыми и должны ли они быть удалены, еслиRemoveEmptyParagraphs указана опция.

```csharp
public bool CleanupParagraphsWithPunctuationMarks { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` .

Вот полный список очищаемых знаков препинания:

* !
* ,
* .
* :
* ;
* ?
* ¡
* ¿

## Примеры

Показывает, как удалить абзацы со знаками препинания после операции слияния писем.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldMergeField mergeFieldOption1 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_1");
mergeFieldOption1.FieldName = "Option_1";

builder.Write(punctuationMark);

FieldMergeField mergeFieldOption2 = (FieldMergeField) builder.InsertField("MERGEFIELD", "Option_2");
mergeFieldOption2.FieldName = "Option_2";

// Настройте свойство «CleanupOptions», чтобы удалить все пустые абзацы, которые создаст это слияние писем.
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyParagraphs;

// Установка свойства «CleanupParagraphsWithPunctuationMarks» в значение «true» также будет учитывать абзацы
// со знаками препинания пустыми, и операция слияния почты также удалит их.
// Установка свойства «CleanupParagraphsWithPunctuationMarks» в значение «false»
// удалит пустые абзацы, кроме абзацев со знаками препинания.
// Это список знаков препинания, к которым относится это свойство: "!", ",", ".", ":", ";", "?", "¡", "¿".
doc.MailMerge.CleanupParagraphsWithPunctuationMarks = cleanupParagraphsWithPunctuationMarks;

doc.MailMerge.Execute(new[] { "Option_1", "Option_2" }, new object[] { null, null });

doc.Save(ArtifactsDir + "MailMerge.RemoveColonBetweenEmptyMergeFields.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
