---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words для .NET
description: Aspose.Words.Lists.ListLevel сорт. Определяет форматирование уровня списка на С#.
type: docs
weight: 3500
url: /ru/net/aspose.words.lists/listlevel/
---
## ListLevel class

Определяет форматирование уровня списка.

Чтобы узнать больше, посетите[Работа со списками](https://docs.aspose.com/words/net/working-with-lists/) статья документации.

```csharp
public class ListLevel
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Получает или задает выравнивание фактического номера элемента списка. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | Получает пользовательский формат числового стиля для этого уровня списка. Например: «a, ç, ĝ, ...». |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Определяет форматирование символов, используемое для метки списка. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Возвращает данные изображения формы маркера изображения для текущего уровня списка. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | True, если уровень преобразует все унаследованные числа в арабский, false, если он сохраняет их нумерационный стиль. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Получает или задает стиль абзаца, связанный с этим уровнем списка. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Возвращает или устанавливает числовой формат для уровня списка. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Возвращает или задает позицию (в пунктах) номера или маркера для уровня списка. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Возвращает или устанавливает стиль номера для этого уровня списка. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Устанавливает или возвращает уровень списка, который должен появиться перед тем, как указанный уровень списка перезапустит нумерацию. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Возвращает или устанавливает начальный номер для этого уровня списка. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Возвращает или устанавливает позицию табуляции (в пунктах) для уровня списка. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Возвращает или задает позицию (в пунктах) второй строки переносимого текста для уровня списка. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Возвращает или задает символ, вставленный после номера уровня списка. |

## Методы

| Имя | Описание |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Создает форму графического маркера для текущего уровня списка. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Удаляет графический маркер для текущего уровня списка. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Сравнивает с указанным ListLevel. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Вычисляет хеш-код для этого объекта. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Сообщает строковое представление`ListLevel`объект для указанного index элемента списка. Параметры определяют[`NumberStyle`](../../aspose.words/numberstyle/) и необязательный формат string , используемый, когдаCustom указано. |

## Примечания

Вы не создаете объекты этого класса. Объекты уровня списка создаются автоматически при создании списка. Вы получаете доступ`ListLevel` объекты через the [`ListLevelCollection`](../listlevelcollection/) коллекция.

Используйте свойства`ListLevel` чтобы указать форматирование списка для отдельных уровней списка.

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

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
