---
title: "Aspose::Words::Replacing::FindReplaceOptions класс"
linktitle: "FindReplaceOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions класс. Указывает параметры для операций поиска/замены. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Указывает параметры операций поиска/замены. Чтобы узнать больше, посетите статью документации [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class FindReplaceOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Инициализирует новый экземпляр класса [FindReplaceOptions](./) с настройками по умолчанию. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Инициализирует новый экземпляр класса [FindReplaceOptions](./) с указанным направлением. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Инициализирует новый экземпляр класса [FindReplaceOptions](./) с указанным обратным вызовом замены. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Инициализирует новый экземпляр класса [FindReplaceOptions](./) с указанным направлением и обратным вызовом замены. |
| [get_ApplyFont](./get_applyfont/)() const | Форматирование текста, применяемое к новому содержимому. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | Форматирование [Paragraph](../../aspose.words/paragraph/) применяемое к новому содержимому. |
| [get_Direction](./get_direction/)() const | Выбирает направление для замены. Значение по умолчанию — [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True указывает, что oldValue должен быть отдельным словом. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри удалённых правок. Значение по умолчанию — **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию — **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию — **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию — **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри вставленных правок. Значение по умолчанию — **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри OfficeMath/>. Значение по умолчанию — **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать фигуры внутри текста. Значение по умолчанию — **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Получает или задает логическое значение, указывающее, следует ли игнорировать содержимое [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). Значение по умолчанию — **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Получает или задает логическое значение, указывающее, что используется старый алгоритм поиска/замены. |
| [get_MatchCase](./get_matchcase/)() const | True указывает на сравнение с учётом регистра, false указывает на сравнение без учёта регистра. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Указывает формат замены. По умолчанию — [Text](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | Пользовательский метод, который вызывается перед каждым вхождением замены. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Получает или задает логическое значение, указывающее, разрешено ли заменять разрыв абзаца, когда нет следующего соседнего абзаца. Значение по умолчанию — **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | Значение true указывает, что поиск текста выполняется последовательно сверху вниз с учётом текстовых полей. Значение по умолчанию — **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Получает или задает логическое значение, указывающее, следует ли распознавать и использовать подстановки в шаблонах замены. Значение по умолчанию — **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Выбирает направление для замены. Значение по умолчанию — [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Указывает формат замены. По умолчанию — [Text](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Пользовательский метод, который вызывается перед каждым вхождением замены. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | Значение true указывает, что поиск текста выполняется последовательно сверху вниз с учётом текстовых полей. Значение по умолчанию — **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Сеттер для [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как переключать чувствительность к регистру при выполнении операции поиска и замены.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "MatchCase" в значение "true", чтобы применять чувствительность к регистру при поиске строк для замены.
// Установите флаг "MatchCase" в значение "false", чтобы игнорировать регистр символов при поиске текста для замены.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Показывает, как переключать операции поиска и замены только отдельными словами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите флаг "FindWholeWordsOnly" в значение "true", чтобы заменять найденный текст, если он не является частью другого слова.
// Установите флаг "FindWholeWordsOnly" в значение "false", чтобы заменять весь текст независимо от его окружения.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## См. также

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
