---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Lists.ListTemplate, содержащее предопределенные форматы списков Microsoft Word, которые позволят вам без труда улучшить представление вашего документа.
type: docs
weight: 3980
url: /ru/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Указывает один из предопределенных форматов списка, доступных в Microsoft Word.

```csharp
public enum ListTemplate
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| BulletDefault | `0` | Маркированный список по умолчанию с 9 уровнями. Маркер первого уровня — диск, маркер второго уровня — круг, маркер третьего уровня — квадрат. Затем форматирование повторяется для оставшихся уровней. |
| BulletDisk | `0` | То же самое, что иBulletDefault. |
| BulletCircle | `1` | Маркер первого уровня - круг. Остальные уровни такие же, как вBulletDefault. |
| BulletSquare | `2` | Маркер первого уровня - квадрат. Остальные уровни такие же, как вBulletDefault. |
| BulletDiamonds | `3` | Пуля первого уровня - 4-алмазный персонаж Wingding. Остальные уровни такие же, как вBulletDefault. |
| BulletArrowHead | `4` | Пуля первого уровня - это наконечник стрелы Wingding. Остальные уровни такие же, как вBulletDefault. |
| BulletTick | `5` | Пуля первого уровня - это символ Wingding. Остальные уровни такие же, как вBulletDefault. |
| NumberDefault | `6` | Нумерованный список по умолчанию с 9 уровнями. Арабская нумерация (1., 2., 3., ...) для первого уровня, нумерация строчными буквами (a., b., c., ...) для второго уровня, строчная римская нумерация (i., ii., iii., ...) для третьего уровня. Затем форматирование повторяется для оставшихся уровней. |
| NumberArabicDot | `6` | То же самое, что иNumberDefault. |
| NumberArabicParenthesis | `7` | Номер первого уровня - "1)". Остальные уровни такие же, как вNumberDefault. |
| NumberUppercaseRomanDot | `8` | Номер первого уровня - "I.". Остальные уровни такие же, как вNumberDefault. |
| NumberUppercaseLetterDot | `9` | Номер первого уровня - "А". Остальные уровни такие же, как вNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Номер первого уровня - "a)". Остальные уровни такие же, как вNumberDefault. |
| NumberLowercaseLetterDot | `11` | Номер первого уровня - "a.". Остальные уровни такие же, как вNumberDefault. |
| NumberLowercaseRomanDot | `12` | Номер первого уровня - "i.". Остальные уровни такие же, как вNumberDefault. |
| OutlineNumbers | `13` | Общий список с уровнями, пронумерованными как «1), a), i), (1), (a), (i), 1., a., i.». |
| OutlineLegal | `14` | Общий список уровней пронумерован как «1., 1.1., 1.1.1, ...». |
| OutlineBullets | `15` | Списки с различными маркерами для разных уровней. |
| OutlineHeadingsArticleSection | `16` | Список структур с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsLegal | `17` | Список структур с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsNumbers | `18` | Список структур с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsChapter | `19` | Список структур с уровнями, связанными со стилями заголовков. |

## Примечания

Значение шаблона списка используется как параметр в the [`Add`](../listcollection/add/) метод.

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков available в диалоговом окне «Маркеры и нумерация» в Microsoft Word 2003.

## Примеры

Показывает, как создать документ, содержащий все шаблоны списков заголовков структуры.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Показывает, как перезапустить нумерацию в списке, скопировав список.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Применим наш список к некоторым абзацам.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// чтобы создать аналогичный список, не внося изменений в оригинал.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Применяем второй список к новым абзацам.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев путем нумерации каждого элемента.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство "ListLevelNumber", мы можем увеличить уровень списка
// для начала автономного подсписка с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
 // Более глубокие уровни списка используют буквы и строчные римские цифры.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// В этом списке перед каждым абзацем будет применен отступ и символ маркера ("•").
// Более глубокие уровни этого списка будут использовать другие символы, такие как «■» и «○».
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Мы можем отключить форматирование списка, чтобы не форматировать последующие абзацы как списки, сняв флаг «Список».
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
