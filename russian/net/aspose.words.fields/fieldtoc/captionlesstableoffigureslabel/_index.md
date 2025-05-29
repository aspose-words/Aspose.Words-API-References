---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldToc CaptionlessTableOfFiguresLabel для настройки таблицы рисунков. Легко управляйте идентификаторами последовательностей без подписей!
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Возвращает или задает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи .

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Примеры

Показывает, как задать имя идентификатора последовательности.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Смотрите также

* class [FieldToc](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
