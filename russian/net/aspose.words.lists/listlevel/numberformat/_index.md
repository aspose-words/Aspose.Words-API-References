---
title: ListLevel.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words для .NET
description: ListLevel NumberFormat свойство. Возвращает или устанавливает числовой формат для уровня списка на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Возвращает или устанавливает числовой формат для уровня списка.

```csharp
public string NumberFormat { get; set; }
```

## Примечания

Среди обычных текстовых символов строка может содержать символы-заполнители от \x0000 до \x0008 , представляющие числа из соответствующих уровней списка.

Например, строка «\x0000.\x0001)» создаст список label , который выглядит примерно так: «1.5)». Число «1» — текущий номер из 1-го уровня списка, число «5» — текущий номер из 2-го уровня списка.

Значение NULL недопустимо, но пустая строка означает, что ни одно число не является допустимым.

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

Показывает усовершенствованные способы настройки меток списков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Метки уровня 1 будут отформатированы в соответствии со стилем абзаца «Заголовок 1» и будут иметь префикс.
// Они будут выглядеть как «Приложение A», «Приложение B»...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Метки уровня 2 будут отображать текущие номера первого и второго уровней списка и иметь ведущие нули.
// Если первый уровень списка равен 1, то метки списков из них будут выглядеть как «Раздел (1.01)», «Раздел (1.02)»...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Обратите внимание, что на более высоком уровне используется нумерация UppercaseLetter.
// Мы можем установить свойство IsLegal для использования арабских цифр для более высоких уровней списка.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Метки уровня 3 будут представлять собой римские цифры в верхнем регистре с префиксом и суффиксом и будут перезапускаться для каждого элемента списка уровня 1.
// Эти метки списка будут выглядеть как "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Сделайте метки всех уровней списка жирными.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Применяем форматирование списка к текущему абзацу.
builder.ListFormat.List = list;

// Создаем элементы списка, которые будут отображать все три уровня нашего списка.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Смотрите также

* class [ListLevel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
