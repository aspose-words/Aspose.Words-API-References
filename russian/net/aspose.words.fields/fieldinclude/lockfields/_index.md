---
title: FieldInclude.LockFields
second_title: Справочник по API Aspose.Words для .NET
description: FieldInclude свойство. Получает или задает следует ли запретить обновление полей во включенном документе.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Получает или задает, следует ли запретить обновление полей во включенном документе.

```csharp
public bool LockFields { get; set; }
```

### Примеры

Показывает, как создать поле INCLUDE и установить его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем использовать поле INCLUDE для импорта части другого документа в локальную файловую систему.
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
* пространство имен [Aspose.Words.Fields](../../fieldinclude/)
* сборка [Aspose.Words](../../../)


