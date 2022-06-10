---
title: FindReplaceOptions
second_title: Справочник по API Aspose.Words для .NET
description: Указывает параметры операций поиска/замены.
type: docs
weight: 4310
url: /ru/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Указывает параметры операций поиска/замены.

```csharp
public class FindReplaceOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions#constructor)() | Конструктор по умолчанию. |
| [FindReplaceOptions](findreplaceoptions#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont) { get; } | Форматирование текста применяется к новому содержимому. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat) { get; } | Форматирование абзаца применяется к новому содержимому. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction) { get; set; } | Выбирает направление замены. Значение по умолчанию:Forward. |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly) { get; set; } | True указывает, что oldValue должно быть отдельным словом. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted) { get; set; } | Получает или задает логическое значение, указывающее либо игнорировать текст внутри удаленных ревизий. Значение по умолчанию:` false` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию:` false` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию:` false` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию:` false` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted) { get; set; } | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри ревизий вставки. Значение по умолчанию:` false` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode) { get; set; } | Получает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase) { get; set; } | True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback) { get; set; } | Определяемый пользователем метод, который вызывается перед каждой заменой. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement) { get; set; } | Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца при отсутствии следующего родственного абзаца. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder) { get; set; } | True указывает, что текстовый поиск выполняется последовательно сверху вниз с учетом текстовых полей. Значение по умолчанию — false. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions) { get; set; } | Получает или задает логическое значение, указывающее, следует ли распознавать и использовать замены в шаблонах замены. Значение по умолчанию:` false` . |

### Примеры

Показывает, как переключить чувствительность к регистру при выполнении операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг "FindWholeWordsOnly" в "true", чтобы заменить найденный текст, если он не является частью другого слова.
// Установите флаг «FindWholeWordsOnly» в «false», чтобы заменить весь текст независимо от его окружения.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Показывает, как переключать автономные операции поиска и замены только для слов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг "FindWholeWordsOnly" в "true", чтобы заменить найденный текст, если он не является частью другого слова.
// Установите флаг «FindWholeWordsOnly» в «false», чтобы заменить весь текст независимо от его окружения.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Смотрите также

* пространство имен [Aspose.Words.Replacing](../../aspose.words.replacing)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
