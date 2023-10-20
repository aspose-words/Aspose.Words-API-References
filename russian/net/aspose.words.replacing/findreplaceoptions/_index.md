---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.Replacing.FindReplaceOptions сорт. Определяет параметры для операций поиска/замены на С#.
type: docs
weight: 4620
url: /ru/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Определяет параметры для операций поиска/замены.

Чтобы узнать больше, посетите[Найти и заменить](https://docs.aspose.com/words/net/find-and-replace/) статья документации.

```csharp
public class FindReplaceOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Конструктор по умолчанию. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) |  |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Форматирование текста, примененное к новому содержимому. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Форматирование абзацев применено к новому содержимому. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Выбирает направление замены. Значение по умолчанию:Forward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True указывает, что oldValue должно быть отдельным словом. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри удаляемых ревизий. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри редакций вставки. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать фигуры в тексте. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать содержимое[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Значение по умолчанию:`ЛОЖЬ` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Получает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Пользовательский метод, который вызывается перед каждой заменой. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Получает или задает логическое значение, указывающее, разрешено ли заменять абзацbreak , если нет следующего одноуровневого абзаца. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчанию:`ЛОЖЬ` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Получает или задает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. Значение по умолчанию:`ЛОЖЬ` . |

## Примеры

Показывает, как переключить чувствительность к регистру при выполнении операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для флага «MatchCase» значение «true», чтобы применять чувствительность к регистру при поиске заменяемых строк.
// Установите флаг «MatchCase» в значение «false», чтобы игнорировать регистр символов при поиске текста для замены.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Показывает, как переключать отдельные операции поиска и замены только по словам.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг «FindWholeWordsOnly» в значение «true», чтобы заменить найденный текст, если он не является частью другого слова.
// Установите для флага «FindWholeWordsOnly» значение «false», чтобы заменить весь текст независимо от его окружения.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Смотрите также

* пространство имен [Aspose.Words.Replacing](../../aspose.words.replacing/)
* сборка [Aspose.Words](../../)
