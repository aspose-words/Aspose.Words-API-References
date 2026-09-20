---
title: "Aspose::Words::NumberStyle перечисление"
linktitle: "NumberStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NumberStyle перечисление. Указывает стиль нумерации для списка, сносок и концевых сносок, номеров страниц в C++."
type: docs
weight: 103000
url: /ru/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Указывает стиль нумерации для списка, сносок и концевых сносок, номеров страниц.

```cpp
enum class NumberStyle
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Арабский | 0 | Арабская нумерация (1, 2, 3, ...) |
| UppercaseRoman | 1 | Римские цифры в верхнем регистре (I, II, III, ...) |
| LowercaseRoman | 2 | Римские цифры в нижнем регистре (i, ii, iii, ...) |
| UppercaseLetter | 3 | Буквы в верхнем регистре (A, B, C, ...) |
| LowercaseLetter | 4 | Буквы в нижнем регистре (a, b, c, ...) |
| Ordinal | 5 | Порядковый (1st, 2nd, 3rd, ...) |
| Number | 6 | Нумерованный (One, Two, Three, ...) |
| OrdinalText | 7 | Порядковый (текст) (First, Second, Third, ...) |
| Шестнадцатеричный | 8 | Шестнадцатеричный: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Руководство Чикаго по [Style](../style/): *, †, † |
| Кандзи | 10 | Идеограф-цифровой. |
| KanjiDigit | 11 | Японский счет. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Полноширинный арабский: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Полуширинный арабский: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Японское правовое. |
| KanjiTraditional2 | 17 | Японская цифровая запись десяти тысяч. |
| NumberInCircle | 18 | Закрытые круги. |
| DecimalFullWidth | 19 | Десятичные символы полной ширины: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo полной ширины. |
| Iroha | 21 | Iroha полной ширины. |
| LeadingZero | 22 | Ведущий ноль (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Маркер (проверьте код символа в тексте) |
| Ganada | 24 | Корейский Ganada. |
| Chosung | 25 | Корея Chosung. |
| GB1 | 26 | Вложенная точка. |
| GB2 | 27 | Вложенная скобка. |
| GB3 | 28 | Вложенный круг китайский. |
| GB4 | 29 | Иероглиф в окружённом круге. |
| Zodiac1 | 30 | Традиционный иероглиф. |
| Zodiac2 | 31 | Иероглиф зодиака. |
| Zodiac3 | 32 | Традиционный иероглиф зодиака. |
| TradChinNum1 | 33 | Тайваньский подсчёт. |
| TradChinNum2 | 34 | Традиционный юридический иероглиф. |
| TradChinNum3 | 35 | Тайваньский подсчёт тысяч. |
| TradChinNum4 | 36 | Тайваньский цифровой. |
| SimpChinNum1 | 37 | Китайский подсчёт. |
| SimpChinNum2 | 38 | Упрощённый юридический китайский. |
| SimpChinNum3 | 39 | Китайский подсчёт тысяч. |
| SimpChinNum4 | 40 | Китайский (не реализовано) |
| HanjaRead | 41 | Корейский цифровой. |
| HanjaReadDigit | 42 | Корейский подсчёт. |
| Hangul | 43 | Корейское право. |
| Hanja | 44 | Корейский цифровой2. |
| Hebrew1 | 45 | Иврит-1. |
| Arabic1 | 46 | Арабский альфа. |
| Hebrew2 | 47 | Иврит-2. |
| Arabic2 | 48 | Арабский абджад. |
| HindiLetter1 | 49 | Хинди гласные. |
| HindiLetter2 | 50 | Согласные хинди. |
| HindiArabic | 51 | Числа хинди. |
| HindiCardinalText | 52 | Хинди описательное (кардиналы) |
| ThaiLetter | 53 | Тайские буквы. |
| ThaiArabic | 54 | Тайские числа. |
| ThaiCardinalText | 55 | Тайское описательное (кардиналы) |
| VietCardinalText | 56 | Вьетнамское описательное (кардиналы) |
| NumberInDash | 57 | Формат номера страницы: - 1 -, - 2 -, - 3 -, - 4 -. |
| LowercaseRussian | 58 | Строчные буквы русского алфавита. |
| UppercaseRussian | 59 | Прописные буквы русского алфавита. |
| None | 255 | Без маркера или номера. |
| Пользовательский | 65280 | Пользовательский числовой формат. Он поддерживается только форматом DOCX. |


## Примеры



Показывает, как применить пользовательское форматирование списка к абзацам при использовании [DocumentBuilder](../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Список позволяет организовывать и оформлять наборы абзацев с помощью префиксных символов и отступов.
// Мы можем создавать вложенные списки, увеличивая уровень отступа.
// Мы можем начинать и завершать список, используя свойство "ListFormat" объекта document builder.
// Каждый абзац, который мы добавляем между началом и концом списка, становится элементом списка.
// Создайте список из шаблона Microsoft Word и настройте первые два уровня списка.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Это значение NumberFormat создаст символы маркеров в виде звёзд.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Создайте абзацы и примените к ним оба уровня нашего пользовательского форматирования списка.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
