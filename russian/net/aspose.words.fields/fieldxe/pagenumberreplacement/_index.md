---
title: FieldXE.PageNumberReplacement
second_title: Справочник по API Aspose.Words для .NET
description: FieldXE свойство. Получает или задает текст используемый вместо номера страницы.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Получает или задает текст, используемый вместо номера страницы.

```csharp
public string PageNumberReplacement { get; set; }
```

### Примеры

Показывает, как определить перекрестные ссылки в поле ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE с левой стороны,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с совпадающими значениями в свойстве "Текст"
// в одну запись вместо создания записи для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Мы можем настроить поле XE, чтобы его запись INDEX отображала строку вместо номера страницы.
// Во-первых, для записей, которые заменяют номер страницы строкой,
// указать пользовательский разделитель между значением свойства Text поля XE и строкой.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Вставляем поле XE, которое создает обычную запись INDEX, которая отображает номер страницы этого поля,
// и не вызывает значение CrossReferenceSeparator.
// Запись для этого поля XE будет отображать «Apple, 2».
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Вставьте еще одно поле XE на страницу 3 и установите значение для свойства PageNumberReplacement.
// Это значение будет отображаться вместо номера страницы, на которой находится это поле,
// и перед ним появится значение CrossReferenceSeparator поля INDEX.
// Запись для этого поля XE будет отображать «Банан, см.: Тропический фрукт».
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Смотрите также

* class [FieldXE](../)
* пространство имен [Aspose.Words.Fields](../../fieldxe/)
* сборка [Aspose.Words](../../../)


