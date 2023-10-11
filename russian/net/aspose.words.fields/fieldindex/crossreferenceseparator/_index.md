---
title: FieldIndex.CrossReferenceSeparator
second_title: Справочник по API Aspose.Words для .NET
description: FieldIndex свойство. Получает или задает последовательность символов которая используется для разделения перекрестных ссылок и других записей.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

Получает или задает последовательность символов, которая используется для разделения перекрестных ссылок и других записей.

```csharp
public string CrossReferenceSeparator { get; set; }
```

### Примеры

Показывает, как определить перекрестные ссылки в поле ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, в котором будет отображаться запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с совпадающими значениями в свойстве «Текст».
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Мы можем настроить поле XE так, чтобы его запись INDEX отображала строку вместо номера страницы.
// Во-первых, для записей, в которых номер страницы заменяется строкой,
// указать пользовательский разделитель между значением свойства Text поля XE и строкой.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Вставка поля XE, при этом создается обычная запись INDEX, отображающая номер страницы этого поля,
// и не вызывает значение CrossReferenceSeparator.
// В этом поле XE будет отображаться «Apple, 2».
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Вставляем еще одно поле XE на странице 3 и устанавливаем значение для свойства PageNumberReplacement.
// Это значение будет отображаться вместо номера страницы, на которой находится это поле,
// и перед ним появится значение CrossReferenceSeparator поля INDEX.
// В этом поле XE будет отображаться «Банан, см.: Тропические фрукты».
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../fieldindex/)
* сборка [Aspose.Words](../../../)


