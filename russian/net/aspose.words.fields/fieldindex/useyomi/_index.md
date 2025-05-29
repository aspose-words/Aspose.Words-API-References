---
title: FieldIndex.UseYomi
linktitle: UseYomi
articleTitle: UseYomi
second_title: Aspose.Words для .NET
description: Улучшите индексацию с помощью свойства FieldIndex UseYomi. Легко включите текст yomi для улучшения видимости поиска и лучшего пользовательского опыта.
type: docs
weight: 170
url: /ru/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

Возвращает или задает, следует ли включить использование текста yomi для записей индекса.

```csharp
public bool UseYomi { get; set; }
```

## Примеры

Показывает, как сортировать записи поля INDEX по фонетике.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с соответствующими значениями в свойстве «Текст»
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Таблица INDEX автоматически сортирует свои записи по значениям их свойств Text в алфавитном порядке.
// Настройте таблицу INDEX для фонетической сортировки записей с использованием хираганы.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Вставьте 4 поля XE, которые будут отображаться как записи в таблице содержания поля INDEX.
// Свойство «Текст» может содержать написание слова на кандзи, произношение которого может быть неоднозначным,
// в то время как версия слова «Ёми» будет писаться точно так же, как оно произносится с использованием хираганы.
// Если мы установим наше поле INDEX на использование Yomi, оно отсортирует эти записи
// по значению их свойств Yomi, а не по их значениям Text.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
