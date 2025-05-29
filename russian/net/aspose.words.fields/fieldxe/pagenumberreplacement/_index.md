---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldXE PageNumberReplacement, позволяющее легко настраивать текст номера страницы для улучшенного форматирования документа и повышения его читабельности.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Возвращает или задает текст, используемый вместо номера страницы.

```csharp
public string PageNumberReplacement { get; set; }
```

## Примеры

Показывает, как определять перекрестные ссылки в поле ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с соответствующими значениями в свойстве «Текст»
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Мы можем настроить поле XE так, чтобы его запись INDEX отображала строку вместо номера страницы.
// Во-первых, для записей, которые заменяют номер страницы строкой,
// укажите пользовательский разделитель между значением свойства Text поля XE и строкой.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Вставьте поле XE, которое создает обычную запись INDEX, отображающую номер страницы этого поля,
// и не вызывает значение CrossReferenceSeparator.
// Запись для этого поля XE будет отображать «Apple, 2».
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Вставьте еще одно поле XE на страницу 3 и задайте значение для свойства PageNumberReplacement.
// Это значение будет отображаться вместо номера страницы, на которой находится это поле,
// и значение CrossReferenceSeparator поля INDEX появится перед ним.
// Запись для этого поля XE будет отображать «Банан, см.: Тропические фрукты».
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

* class [FieldXE](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
