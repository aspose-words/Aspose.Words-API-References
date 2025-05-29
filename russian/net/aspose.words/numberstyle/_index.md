---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.NumberStyle для настройки номеров страниц сносок и концевых сносок, что позволит без труда улучшить форматирование документа.
type: docs
weight: 5040
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
| UppercaseRoman | `1` | Заглавные римские буквы (I, II, III, ...) |
| LowercaseRoman | `2` | Строчные римские буквы (i, ii, iii, ...) |
| UppercaseLetter | `3` | Заглавная буква (A, B, C, ...) |
| LowercaseLetter | `4` | Строчная буква (a, b, c, ...) |
| Ordinal | `5` | Порядковый номер (1-й, 2-й, 3-й, ...) |
| Number | `6` | Пронумерованный (Один, Два, Три, ...) |
| OrdinalText | `7` | Порядковый (текст) (Первый, Второй, Третий, ...) |
| Hex | `8` | Шестнадцатеричное: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Чикагское руководство по стилю: *, †, † |
| Kanji | `10` | Идеограф-цифровой |
| KanjiDigit | `11` | Японский счет |
| AiueoHalfWidth | `12` | Айуэо |
| IrohaHalfWidth | `13` | Ироха |
| ArabicFullWidth | `14` | Полноширинные арабские буквы: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Полуширинные арабские: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Японский легальный |
| KanjiTraditional2 | `17` | Японский цифровой десять тысяч |
| NumberInCircle | `18` | Замкнутые круги |
| DecimalFullWidth | `19` | Десятичная полная ширина: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo полная ширина |
| Iroha | `21` | Ироха полная ширина |
| LeadingZero | `22` | Начальный ноль (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Пуля (проверьте код символа в тексте) |
| Ganada | `24` | Корейская Ганада |
| Chosung | `25` | Корея Чосон |
| GB1 | `26` | Закрытая точка |
| GB2 | `27` | Закрытые скобки |
| GB3 | `28` | Замкнутый круг Китайский |
| GB4 | `29` | Идеограмма замкнутый круг |
| Zodiac1 | `30` | Идеограмма традиционная |
| Zodiac2 | `31` | Идеографический знак Зодиака |
| Zodiac3 | `32` | Идеографический Зодиак традиционный |
| TradChinNum1 | `33` | Тайваньский счет |
| TradChinNum2 | `34` | Идеограмма законная традиционная |
| TradChinNum3 | `35` | Тайваньцы считают тысячи |
| TradChinNum4 | `36` | Тайваньский цифровой |
| SimpChinNum1 | `37` | Китайский счет |
| SimpChinNum2 | `38` | Китайский юридический упрощенный |
| SimpChinNum3 | `39` | Китайский счет тысяч |
| SimpChinNum4 | `40` | Китайский (не реализовано) |
| HanjaRead | `41` | Корейский цифровой |
| HanjaReadDigit | `42` | Корейский счет |
| Hangul | `43` | Корея легально |
| Hanja | `44` | Корея digital2 |
| Hebrew1 | `45` | Иврит-1 |
| Arabic1 | `46` | Арабский алфавит |
| Hebrew2 | `47` | Иврит-2 |
| Arabic2 | `48` | Арабский абджад |
| HindiLetter1 | `49` | Гласные хинди |
| HindiLetter2 | `50` | Согласные хинди |
| HindiArabic | `51` | Числа на хинди |
| HindiCardinalText | `52` | Хинди описательные (количественные числительные) |
| ThaiLetter | `53` | Тайские буквы |
| ThaiArabic | `54` | Тайские цифры |
| ThaiCardinalText | `55` | Тайский описательный (кардинальный) |
| VietCardinalText | `56` | Вьетнамские описательные (кардинальные) |
| NumberInDash | `57` | Формат номера страницы: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Строчные буквы русского алфавита |
| UppercaseRussian | `59` | Заглавные буквы русского алфавита |
| None | `255` | Нет маркера или номера. |
| Custom | `65280` | Пользовательский формат числа. Поддерживается только форматом DOCX. |

## Примеры

Показывает, как применять пользовательское форматирование списка к абзацам при использовании DocumentBuilder.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
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

// Создаем абзацы и применяем к ним оба уровня списка нашего пользовательского форматирования.
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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
