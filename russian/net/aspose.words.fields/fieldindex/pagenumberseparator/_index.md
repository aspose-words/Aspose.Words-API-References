---
title: FieldIndex.PageNumberSeparator
linktitle: PageNumberSeparator
articleTitle: PageNumberSeparator
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldIndex PageNumberSeparator, легко настройте символ, разделяющий записи индекса от номеров страниц для большей ясности.
type: docs
weight: 120
url: /ru/net/aspose.words.fields/fieldindex/pagenumberseparator/
---
## FieldIndex.PageNumberSeparator property

Возвращает или задает последовательность символов, которая используется для разделения записи индекса и ее номера страницы.

```csharp
public string PageNumberSeparator { get; set; }
```

## Примеры

Показывает, как редактировать разделитель номеров страниц в поле ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX сгруппирует поля XE с соответствующими значениями в свойстве «Текст»
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Если наше поле INDEX имеет запись для группы полей XE,
// эта запись отобразит номер каждой страницы, содержащей поле XE, принадлежащее этой группе.
// Мы можем установить пользовательские разделители, чтобы настроить внешний вид этих номеров страниц.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// После вставки этих полей XE поле ИНДЕКС отобразит «Первая запись на страницах 2, 3 и 4».
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
