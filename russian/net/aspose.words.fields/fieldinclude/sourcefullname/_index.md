---
title: FieldInclude.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство FieldInclude SourceFullName для эффективного управления местоположениями документов. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldinclude/sourcefullname/
---
## FieldInclude.SourceFullName property

Возвращает или задает местоположение документа.

```csharp
public string SourceFullName { get; set; }
```

## Примеры

Показывает, как создать поле INCLUDE и задать его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем использовать поле INCLUDE для импорта части другого документа в локальной файловой системе.
// Закладка из другого документа, на который мы ссылаемся с помощью этого поля, содержит эту импортированную часть.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Смотрите также

* class [FieldInclude](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
