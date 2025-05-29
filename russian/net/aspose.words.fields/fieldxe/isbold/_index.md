---
title: FieldXE.IsBold
linktitle: IsBold
articleTitle: IsBold
second_title: Aspose.Words для .NET
description: Улучшите свой опыт работы с FieldXE! Управляйте жирным форматированием для номеров страниц ввода без усилий с помощью свойства IsBold. Повысьте читабельность и стиль!
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldxe/isbold/
---
## FieldXE.IsBold property

Возвращает или задает, следует ли применять полужирное форматирование к номеру страницы записи.

```csharp
public bool IsBold { get; set; }
```

## Примеры

Показывает, как заполнить поле INDEX записями с использованием полей XE, а также изменить его внешний вид.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве "Текст",
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Установка значения этого свойства на «A» сгруппирует все записи по первой букве,
// и поместите эту букву в верхнем регистре над каждой группой.
index.Heading = "A";

// Задаем таблицу, созданную по полю INDEX, так, чтобы она охватывала 2 столбца.
index.NumberOfColumns = "2";

// Устанавливает, что все записи, начинающиеся с букв, выходящих за пределы диапазона символов «ac», должны быть пропущены.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Следующие два поля XE будут отображаться под заголовком «A»,
// с соответствующими стилями текста, также примененными к номерам страниц.
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

// Следующие два поля XE будут находиться под заголовками «B» и «C» в таблице содержания полей INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// Поля INDEX сортируют все записи в алфавитном порядке, поэтому эта запись будет отображаться под буквой «A» вместе с двумя другими.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Эта запись не будет отображаться, так как она начинается с буквы «D»,
// который находится за пределами диапазона символов «ac», определяемого свойством LetterRange поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Смотрите также

* class [FieldXE](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
