---
title: ListTemplate
second_title: Справочник по API Aspose.Words для .NET
description: Указывает один из предопределенных форматов списка доступных в Microsoft Word.
type: docs
weight: 3280
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
| BulletDefault | `0` | Маркированный список по умолчанию с 9 уровнями. Пуля первого уровня — диск, пуля второго уровня — круг, пуля третьего уровня — квадрат. Затем форматирование повторяется для остальных уровней. |
| BulletDisk | `0` | То же, что и BulletDefault. |
| BulletCircle | `1` | Пуля первого уровня - круг. Остальные уровни такие же, как в BulletDefault. |
| BulletSquare | `2` | Пуля первого уровня - квадратная. Остальные уровни такие же, как в BulletDefault. |
| BulletDiamonds | `3` | Пуля первого уровня - 4-х алмазный персонаж Wingding. Остальные уровни такие же, как в BulletDefault. |
| BulletArrowHead | `4` | Пуля первого уровня представляет собой наконечник стрелы Крылатого персонажа. Остальные уровни такие же, как в BulletDefault. |
| BulletTick | `5` | Пуля первого уровня - это тик Крылатый персонаж. Остальные уровни такие же, как в BulletDefault. |
| NumberDefault | `6` | Нумерованный список по умолчанию с 9 уровнями. арабская нумерация (1., 2., 3., ...) для первого уровня, нумерация строчными буквами (a., b., c., ...) для второго уровня, строчная римская нумерация (i., ii., iii., ...) для третьего уровня. Затем форматирование повторяется для остальных уровней. |
| NumberArabicDot | `6` | То же, что и NumberDefault. |
| NumberArabicParenthesis | `7` | Номер первого уровня "1)". Остальные уровни такие же, как в NumberDefault. |
| NumberUppercaseRomanDot | `8` | Номер первого уровня "I.". Остальные уровни такие же, как в NumberDefault. |
| NumberUppercaseLetterDot | `9` | Номер первого уровня "A.". Остальные уровни такие же, как в NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Номер первого уровня "a)". Остальные уровни такие же, как в NumberDefault. |
| NumberLowercaseLetterDot | `11` | Номер первого уровня "a.". Остальные уровни такие же, как в NumberDefault. |
| NumberLowercaseRomanDot | `12` | Номер первого уровня "i.". Остальные уровни такие же, как в NumberDefault. |
| OutlineNumbers | `13` | Список структур с уровнями, пронумерованными "1", a), i), (1), (a), (i), 1., a., я.". |
| OutlineLegal | `14` | Список структур с уровнями нумеруется "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | Списки с различными маркерами для разных уровней. |
| OutlineHeadingsArticleSection | `16` | Список структур с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsLegal | `17` | Список структур с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsNumbers | `18` | Список структур с уровнями, связанными со стилями заголовков. |
| OutlineHeadingsChapter | `19` | Список структур с уровнями, связанными со стилями заголовков. |

### Примечания

Значение шаблона списка используется как параметр в [`Add`](../listcollection/add)метод.

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков, доступным в диалоговом окне Маркеры и нумерация в Microsoft Word 2003.

### Примеры

Показывает, как создать документ, содержащий все шаблоны списка структурных заголовков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
 // Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
 // 1 - Нумерованный список:
 // Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // Установив свойство "ListLevelNumber", мы можем увеличить список level
 // чтобы начать автономный подсписок с текущего элемента списка.
 // Шаблон списка Microsoft Word под названием "NumberDefault" использует числа для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и строчные римские цифры. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 2 - Маркированный список: 
 // Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
 // На более глубоких уровнях этого списка будут использоваться другие символы, такие как "■" и "○".
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

Показывает, как перезапустить нумерацию в списке путем копирования списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
 // Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
 // 1 - Нумерованный список:
 // Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // Установив свойство "ListLevelNumber", мы можем увеличить список level
 // чтобы начать автономный подсписок с текущего элемента списка.
 // Шаблон списка Microsoft Word под названием "NumberDefault" использует числа для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и строчные римские цифры. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 2 - Маркированный список: 
 // Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
 // На более глубоких уровнях этого списка будут использоваться другие символы, такие как "■" и "○".
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

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
 // Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
 // 1 - Нумерованный список:
 // Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // Установив свойство "ListLevelNumber", мы можем увеличить список level
 // чтобы начать автономный подсписок с текущего элемента списка.
 // Шаблон списка Microsoft Word под названием "NumberDefault" использует числа для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и строчные римские цифры. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

 // 2 - Маркированный список: 
 // Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
 // На более глубоких уровнях этого списка будут использоваться другие символы, такие как "■" и "○".
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

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
