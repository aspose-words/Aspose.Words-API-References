---
title: NumberStyle
second_title: Справочник по API Aspose.Words для .NET
description: Задает стиль нумерации для списка сносок и концевых сносок номеров страниц.
type: docs
weight: 4020
url: /ru/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Задает стиль нумерации для списка, сносок и концевых сносок, номеров страниц.

```csharp
public enum NumberStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Arabic | `0` | Арабская нумерация (1, 2, 3, ...) |
| UppercaseRoman | `1` | Верхний регистр Roman (I, II, III, ...) |
| LowercaseRoman | `2` | Строчные латинские буквы (i, ii, iii, ...) |
| UppercaseLetter | `3` | Заглавная буква (A, B, C, ...) |
| LowercaseLetter | `4` | Строчная буква (a, b, c, ...) |
| Ordinal | `5` | Порядковый номер (1-й, 2-й, 3-й, ...) |
| Number | `6` | Нумерованные (один, два, три, ...) |
| OrdinalText | `7` | Порядковый номер (текст) (первый, второй, третий, ...) |
| Hex | `8` | Шестнадцатеричный:8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Чикагское руководство по стилю:*, †, † |
| Kanji | `10` | Идеограф-цифровой |
| KanjiDigit | `11` | Японский счет |
| AiueoHalfWidth | `12` | Айуэо |
| IrohaHalfWidth | `13` | Ироха |
| ArabicFullWidth | `14` | Полноширинный арабский:1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Полуширинный арабский:1, 2, 3, 4 |
| KanjiTraditional | `16` | Японский юридический |
| KanjiTraditional2 | `17` | Японские цифровые десять тысяч |
| NumberInCircle | `18` | Замкнутые круги |
| DecimalFullWidth | `19` | Десятичная полная ширина:1, 2, 3, 4 |
| Aiueo | `20` | Aiueo полная ширина |
| Iroha | `21` | Ироха полная ширина |
| LeadingZero | `22` | Ведущий ноль (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Bullet (проверьте код символа в тексте) |
| Ganada | `24` | Корейская Ганада |
| Chosung | `25` | Корея Чосон |
| GB1 | `26` | Закрытая точка |
| GB2 | `27` | Круглые скобки |
| GB3 | `28` | Замкнутый круг Китайский |
| GB4 | `29` | Идеограф в замкнутом круге |
| Zodiac1 | `30` | Идеография традиционная |
| Zodiac2 | `31` | Идеограф Зодиак |
| Zodiac3 | `32` | Идеографический Зодиак традиционный |
| TradChinNum1 | `33` | Тайваньский счет |
| TradChinNum2 | `34` | Идеография правовая традиционная |
| TradChinNum3 | `35` | Тайваньский счет тысяч |
| TradChinNum4 | `36` | Тайваньский цифровой |
| SimpChinNum1 | `37` | Китайский счет |
| SimpChinNum2 | `38` | Юридический упрощенный китайский |
| SimpChinNum3 | `39` | Китайский счет тысяч |
| SimpChinNum4 | `40` | Китайский (не реализовано) |
| HanjaRead | `41` | Корейский цифровой |
| HanjaReadDigit | `42` | Корейский счет |
| Hangul | `43` | Законы Кореи |
| Hanja | `44` | Корея цифровая2 |
| Hebrew1 | `45` | Иврит-1 |
| Arabic1 | `46` | Арабская альфа |
| Hebrew2 | `47` | Иврит-2 |
| Arabic2 | `48` | арабский абджад |
| HindiLetter1 | `49` | Гласные хинди |
| HindiLetter2 | `50` | Согласные хинди |
| HindiArabic | `51` | Числа на хинди |
| HindiCardinalText | `52` | Описательный хинди (кардиналы) |
| ThaiLetter | `53` | Тайские буквы |
| ThaiArabic | `54` | Тайские числа |
| ThaiCardinalText | `55` | Тайский описательный (кардиналы) |
| VietCardinalText | `56` | Описательный вьетнамский (кардиналы) |
| NumberInDash | `57` | Формат номера страницы:- 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Строчные буквы русского алфавита |
| UppercaseRussian | `59` | Русский алфавит в верхнем регистре |
| None | `255` | Нет маркера или номера. |
| Custom | `65280` | Пользовательский числовой формат. Поддерживается только форматом DOCX. |

### Примеры

Показывает, как применять форматирование пользовательского списка к абзацам при использовании DocumentBuilder.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
 // Создайте список из шаблона Microsoft Word и настройте первые два уровня списка.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

 // Это значение NumberFormat создаст символы маркированного списка в форме звезды.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

 // Создаем абзацы и применяем к ним оба уровня списка нашего пользовательского форматирования списка.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Смотрите также

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
