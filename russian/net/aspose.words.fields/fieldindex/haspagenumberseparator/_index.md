---
title: FieldIndex.HasPageNumberSeparator
second_title: Справочник по API Aspose.Words для .NET
description: FieldIndex свойство. Получает значение указывающее переопределяется ли разделитель номеров страниц кодом поля.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldindex/haspagenumberseparator/
---
## FieldIndex.HasPageNumberSeparator property

Получает значение, указывающее, переопределяется ли разделитель номеров страниц кодом поля.

```csharp
public bool HasPageNumberSeparator { get; }
```

### Примеры

Показывает, как редактировать разделитель номеров страниц в поле ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE с левой стороны,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX сгруппирует поля XE с соответствующими значениями в свойстве "Текст"
// в одну запись вместо создания записи для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Если в нашем поле INDEX есть запись для группы полей XE,
// эта запись будет отображать номер каждой страницы, содержащей поле XE, принадлежащее этой группе.
// Мы можем установить пользовательские разделители, чтобы настроить внешний вид этих номеров страниц.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// После того, как мы вставим эти поля XE, в поле ИНДЕКС будет отображаться «Первая запись, на страницах 2, 3 и 4».
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

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../fieldindex/)
* сборка [Aspose.Words](../../../)


