---
title: ListTrailingCharacter Enum
linktitle: ListTrailingCharacter
articleTitle: ListTrailingCharacter
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Lists.ListTrailingCharacter, чтобы настраивать метки списков и улучшать форматирование абзацев для безупречного представления документа.
type: docs
weight: 3990
url: /ru/net/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enumeration

Указывает символ, который отделяет метку списка от текста абзаца.

```csharp
public enum ListTrailingCharacter
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Tab | `0` | Символ табуляции помещается между меткой списка и текстом абзаца. |
| Space | `1` | Между меткой списка и текстом абзаца ставится пробел. |
| Nothing | `2` | Между меткой списка и текстом абзаца нет разделительного символа. |

## Примечания

Используется как значение для[`TrailingCharacter`](../listlevel/trailingcharacter/) свойство.

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

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
