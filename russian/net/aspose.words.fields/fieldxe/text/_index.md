---
title: Text
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает текст записи.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Получает или задает текст записи.

```csharp
public string Text { get; set; }
```

### Примеры

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE с левой стороны
// и страница, содержащая поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве «Текст»,
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Настройте поле INDEX только для отображения полей XE, которые находятся в пределах границ
// закладки с именем "MainBookmark", чьи свойства "EntryType" имеют значение "A".
// Для полей INDEX и XE свойство EntryType использует только первый символ своего строкового значения.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// На новой странице запускаем закладку с именем, совпадающим со значением
// свойства "ИмяЗакладки" поля ИНДЕКС.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Поле ИНДЕКС выберет эту запись, потому что она находится внутри закладки,
// и его тип записи также соответствует типу записи поля INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Вставьте поле XE, которое не будет отображаться в ИНДЕКСЕ, поскольку типы записей не совпадают.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Завершить закладку и затем вставить поле XE.
// Оно того же типа, что и поле ИНДЕКС, но не будет отображаться
// так как он находится за пределами закладки.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Показывает, как заполнить поле INDEX записями, используя поля XE, а также изменить его внешний вид.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE с левой стороны,
// и номер страницы, содержащей поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве «Текст»,
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Установка значения этого свойства в "A" сгруппирует все записи по их первой букве,
// и поместите эту букву в верхнем регистре над каждой группой.
index.Heading = "A";

// Устанавливаем таблицу, созданную полем INDEX, на 2 столбца.
index.NumberOfColumns = "2";

// Установить, что любые записи с начальными буквами за пределами диапазона символов "ac" должны быть опущены.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Следующие два поля XE будут отображаться под заголовком «A»,
// с их соответствующими стилями текста, которые также применяются к их номерам страниц.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Оба следующих двух поля XE будут под заголовками "B" и "C" в таблице содержания полей INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Поля ИНДЕКС сортируют все записи в алфавитном порядке, поэтому эта запись будет отображаться под буквой «А» вместе с двумя другими.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Эта запись не появится, потому что она начинается с буквы "D",
// который находится за пределами диапазона символов "ac", определяемого свойством LetterRange поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Смотрите также

* class [FieldXE](../../fieldxe)
* пространство имен [Aspose.Words.Fields](../../fieldxe)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
