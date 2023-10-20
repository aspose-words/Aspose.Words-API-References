---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words для .NET
description: Aspose.Words.NumberStyle перечисление. Определяет стиль нумерации для списка сносок и концевых сносок номеров страниц на С#.
type: docs
weight: 4310
url: /ru/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

Определяет стиль нумерации для списка, сносок и концевых сносок, номеров страниц.

```csharp
public enum NumberStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Arabic | `0` | Арабская нумерация (1, 2, 3, ...) |
| UppercaseRoman | `1` | Прописные латинские буквы (I, II, III, ...) |
| LowercaseRoman | `2` | Строчные латинские буквы (i, ii, iii, ...) |
| UppercaseLetter | `3` | Прописная буква (A, B, C, ...) |
| LowercaseLetter | `4` | Строчная буква (a, b, c, ...) |
| Ordinal | `5` | Порядковый номер (1-й, 2-й, 3-й, ...) |
| Number | `6` | Пронумеровано (Один, Два, Три, ...) |
| OrdinalText | `7` | Порядковый номер (текст) (первый, второй, третий, ...) |
| Hex | `8` | Шестнадцатеричный: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| ChicagoManual | `9` | Чикагское руководство по стилю: *, †, † |
| Kanji | `10` | Идеограф-цифровой |
| KanjiDigit | `11` | Японский счёт |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | Ироха |
| ArabicFullWidth | `14` | Полноширинный арабский: 1, 2, 3, 4 |
| ArabicHalfWidth | `15` | Полуширина арабского языка: 1, 2, 3, 4 |
| KanjiTraditional | `16` | Японская юридическая информация |
| KanjiTraditional2 | `17` | Японские цифровые десять тысяч |
| NumberInCircle | `18` | Замкнутые круги |
| DecimalFullWidth | `19` | Десятичная полная ширина: 1, 2, 3, 4 |
| Aiueo | `20` | Aiueo полная ширина |
| Iroha | `21` | Ироха полная ширина |
| LeadingZero | `22` | Ведущий ноль (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | `23` | Маркер (проверьте код символа в тексте) |
| Ganada | `24` | Корейская Ганада |
| Chosung | `25` | Корея Чосон |
| GB1 | `26` | Закрытая точка |
| GB2 | `27` | Закрытая скобка |
| GB3 | `28` | Замкнутый круг Chinese |
| GB4 | `29` | Идеограмма в круге |
| Zodiac1 | `30` | Идеограф традиционный |
| Zodiac2 | `31` | Идеограф Зодиака |
| Zodiac3 | `32` | Иероглиф Зодиака традиционный |
| TradChinNum1 | `33` | Тайваньский счет |
| TradChinNum2 | `34` | Иероглиф юридический традиционный |
| TradChinNum3 | `35` | Тайваньцы считают тысячу |
| TradChinNum4 | `36` | Тайваньский цифровой |
| SimpChinNum1 | `37` | Китайский счет |
| SimpChinNum2 | `38` | Упрощенное китайское законодательство |
| SimpChinNum3 | `39` | Китайский счет тысяч |
| SimpChinNum4 | `40` | Китайский (не реализовано) |
| HanjaRead | `41` | Корейский цифровой |
| HanjaReadDigit | `42` | Корейский счет |
| Hangul | `43` | Юридическая информация в Корее |
| Hanja | `44` | Корея digital2 |
| Hebrew1 | `45` | Иврит-1 |
| Arabic1 | `46` | арабский алфавит |
| Hebrew2 | `47` | Иврит-2 |
| Arabic2 | `48` | арабский abjad |
| HindiLetter1 | `49` | Гласные хинди |
| HindiLetter2 | `50` | Согласные хинди |
| HindiArabic | `51` | Числа на хинди |
| HindiCardinalText | `52` | Описательное описание на хинди (кардиналы) |
| ThaiLetter | `53` | Тайские буквы |
| ThaiArabic | `54` | Тайские номера |
| ThaiCardinalText | `55` | Тайское описательное (кардиналы) |
| VietCardinalText | `56` | Вьетнамское описательное (кардиналы) |
| NumberInDash | `57` | Формат номера страницы: - 1 -, - 2 -, - 3 -, - 4 - |
| LowercaseRussian | `58` | Строчный русский алфавит |
| UppercaseRussian | `59` | Русский алфавит верхнего регистра |
| None | `255` | Нет маркера или номера. |
| Custom | `65280` | Пользовательский числовой формат. Поддерживается только форматом DOCX. |

## Примеры

Показывает, как применить пользовательское форматирование списка к абзацам при использовании DocumentBuilder.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Создайте список из шаблона Microsoft Word и настройте первые два уровня его списка.
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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
