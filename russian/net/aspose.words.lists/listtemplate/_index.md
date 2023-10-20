---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words для .NET
description: Aspose.Words.Lists.ListTemplate перечисление. Указывает один из предопределенных форматов списка доступных в Microsoft Word на С#.
type: docs
weight: 3530
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
| BulletDefault | `0` | Маркированный список по умолчанию с 9 уровнями. Пуля первого уровня - диск, Пуля второго уровня - круг, пуля третьего уровня - квадрат. Далее форматирование повторяется для остальных уровней. |
| BulletDisk | `0` | Такой же какBulletDefault. |
| BulletCircle | `1` | Пуля первого уровня представляет собой круг. Остальные уровни такие же, как и вBulletDefault. |
| BulletSquare | `2` | Пуля первого уровня представляет собой квадрат. Остальные уровни такие же, как и вBulletDefault. |
| BulletDiamonds | `3` | Пуля первого уровня - 4-х алмазный персонаж Wingding. Остальные уровни такие же, как и вBulletDefault. |
| BulletArrowHead | `4` | Пуля первого уровня представляет собой наконечник стрелы персонажа Wingding. Остальные уровни такие же, как и вBulletDefault. |
| BulletTick | `5` | Пуля первого уровня представляет собой галочку персонажа Wingding. Остальные уровни такие же, как и вBulletDefault. |
| NumberDefault | `6` | Нумерованный список по умолчанию с 9 уровнями. Арабская нумерация (1., 2., 3., ...) для первого уровня, нумерация строчных букв (a., b., c., ...) для второго уровня, строчная римская нумерация (i ., ii., iii., ...) для третьего уровня. Затем форматирование повторяется для остальных уровней. |
| NumberArabicDot | `6` | Такой же какNumberDefault. |
| NumberArabicParenthesis | `7` | Номер первого уровня — «1)». Остальные уровни такие же, как и вNumberDefault. |
| NumberUppercaseRomanDot | `8` | Число первого уровня – «И.». Остальные уровни такие же, как и вNumberDefault. |
| NumberUppercaseLetterDot | `9` | Число первого уровня – «А». Остальные уровни такие же, как и вNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Номер первого уровня — «а)». Остальные уровни такие же, как и вNumberDefault. |
| NumberLowercaseLetterDot | `11` | Число первого уровня — «а». Остальные уровни такие же, как и вNumberDefault. |
| NumberLowercaseRomanDot | `12` | Число первого уровня – «i». Остальные уровни такие же, как и вNumberDefault. |
| OutlineNumbers | `13` | Контурный список с уровнями, пронумерованными «1), а), i), (1), (a), (i), 1., a., i.». |
| OutlineLegal | `14` | Контурный список с уровнями нумеруется «1., 1.1., 1.1.1, ...». |
| OutlineBullets | `15` | В общих чертах перечислены различные маркеры для разных уровней. |
| OutlineHeadingsArticleSection | `16` | Контурный список с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsLegal | `17` | Контурный список с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsNumbers | `18` | Контурный список с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsChapter | `19` | Контурный список с уровнями, связанными со стилями заголовков. |

## Примечания

Значение шаблона списка используется в качестве параметра в the .[`Add`](../listcollection/add/) метод.

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков Available в диалоговом окне «Маркеры и нумерация» в Microsoft Word 2003.

## Примеры

Показывает, как создать документ, содержащий все шаблоны списков структурных заголовков.

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

Показывает, как возобновить нумерацию в списке путем копирования списка.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Применяем наш список к некоторым абзацам.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// для создания аналогичного списка без внесения изменений в исходный.
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

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев путем нумерации каждого элемента.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство ListLevelNumber, мы можем повысить уровень списка
// чтобы начать автономный подсписок с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
 // На более глубоких уровнях списка используются буквы и строчные римские цифры.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// Этот список будет применять отступ и символ маркера («•») перед каждым абзацем.
// На более глубоких уровнях этого списка будут использоваться другие символы, например «■» и «○».
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
