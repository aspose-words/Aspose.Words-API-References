---
title: Class List
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Lists.List сорт. Представляет форматирование списка.
type: docs
weight: 3260
url: /ru/net/aspose.words.lists/list/
---
## List class

Представляет форматирование списка.

```csharp
public class List : IComparable<List>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Получает документ владельца. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Возвращает true, если этот список является определением стиля списка. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Возвращает true, если этот список является ссылкой на стиль списка. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Возвращает true, если список содержит 9 уровней; false при 1 уровне. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Указывает, следует ли перезапускать список в каждом разделе. Значение по умолчанию: **ЛОЖЬ** . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Получает уникальный идентификатор списка. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Получает набор уровней списка для этого списка. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Получает стиль списка, на который ссылается или определяет этот список. |

## Методы

| Имя | Описание |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(List) | Сравнивает указанный список с текущим списком. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(object) | Сравнивает указанный объект с текущим объектом. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(List) | Сравнивает с указанным списком. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(object) |  |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Вычисляет хэш-код для этого объекта списка. |

### Примечания

Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Каждый список может иметь до 9 уровней, а свойства форматирования, такие как стиль чисел, начальное значение, отступ, позиция табуляции и т. д., определяются отдельно для каждого уровня.

А`List` объект всегда принадлежит[`ListCollection`](../listcollection/) коллекция.

Чтобы создать новый список, используйте методы Add класса[`ListCollection`](../listcollection/) коллекция.

Чтобы изменить форматирование списка, используйте[`ListLevel`](../listlevel/) объекты, найденные в [`ListLevels`](./listlevels/) коллекция.

Чтобы применить или удалить форматирование списка из абзаца, используйте[`ListFormat`](../listformat/).

### Примеры

Показывает, как перезапустить нумерацию в списке путем копирования списка.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
// Мы можем создавать вложенные списки, увеличивая уровень отступа. 
// Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Создайте список из шаблона Microsoft Word и настройте его первый уровень списка.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Применяем наш список к некоторым абзацам.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Мы можем добавить копию существующего списка в коллекцию списков документа
// для создания аналогичного списка без внесения изменений в исходный.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Применяем второй список к новым абзацам.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Показывает, как применить форматирование пользовательского списка к абзацам при использовании DocumentBuilder.

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

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
// Мы можем создавать вложенные списки, увеличивая уровень отступа. 
// Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство "ListLevelNumber", мы можем увеличить уровень списка
// чтобы начать автономный подсписок с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и строчные римские цифры. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
// На более глубоких уровнях этого списка будут использоваться другие символы, такие как "■" и "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Мы можем отключить форматирование списка, чтобы не форматировать последующие абзацы как списки, сняв флаг «Список».
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)


