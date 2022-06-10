---
title: Add
second_title: Справочник по API Aspose.Words для .NET
description: Создает новый список на основе предопределенного шаблона и добавляет его в коллекцию списков в документе.
type: docs
weight: 40
url: /ru/net/aspose.words.lists/listcollection/add/
---
## Add(ListTemplate) {#add}

Создает новый список на основе предопределенного шаблона и добавляет его в коллекцию списков в документе.

```csharp
public List Add(ListTemplate listTemplate)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| listTemplate | ListTemplate | Шаблон списка. |

### Возвращаемое значение

Недавно созданный список.

### Примечания

Шаблоны списков Aspose.Words соответствуют 21 шаблону списков, доступным в диалоговом окне "Маркеры и нумерация" в Microsoft Word 2003.

Все списки, созданные с помощью этого метода, имеют 9 уровней списков.

### Примеры

Показывает, как создать список, применив новый формат списка к набору абзацев.

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
 // Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // Установив свойство "ListLevelNumber", мы можем увеличить список level
 // чтобы начать автономный подсписок с текущего элемента списка.
 // Шаблон списка Microsoft Word под названием "NumberDefault" использует числа для создания уровней списка для первого уровня списка.
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

Показывает, как перезапустить нумерацию в списке путем копирования списка.

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
 // Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // Установив свойство "ListLevelNumber", мы можем увеличить список level
 // чтобы начать автономный подсписок с текущего элемента списка.
 // Шаблон списка Microsoft Word под названием "NumberDefault" использует числа для создания уровней списка для первого уровня списка.
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
 // Нумерованные списки создают логический порядок для своих абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

 // Установив свойство "ListLevelNumber", мы можем увеличить список level
 // чтобы начать автономный подсписок с текущего элемента списка.
 // Шаблон списка Microsoft Word под названием "NumberDefault" использует числа для создания уровней списка для первого уровня списка.
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

* class [List](../../list)
* enum [ListTemplate](../../listtemplate)
* class [ListCollection](../../listcollection)
* namespace [Aspose.Words.Lists](../../listcollection)
* assembly [Aspose.Words](../../../)

---

## Add(Style) {#add_1}

Создает новый список, ссылающийся на стиль списка, и добавляет его в коллекцию списков в документе.

```csharp
public List Add(Style listStyle)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| listStyle | Style | Стиль списка. |

### Возвращаемое значение

Недавно созданный список.

### Примечания

Вновь созданный список ссылается на стиль списка. Если вы измените свойства списка style, это отразится на свойствах списка. И наоборот, если вы измените свойства списка, это отразится на свойствах стиля списка.

### Примеры

Показывает, как создать стиль списка и использовать его в документе.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Мы можем содержать весь объект List в стиле.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

 // Изменяем внешний вид всех уровней списка в нашем списке.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

 // Создать другой список из списка внутри стиля.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

 // Добавляем несколько элементов списка, которые будут форматировать наш список.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

 // Создать и применить другой список на основе стиля списка.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Смотрите также

* class [List](../../list)
* class [Style](../../../aspose.words/style)
* class [ListCollection](../../listcollection)
* namespace [Aspose.Words.Lists](../../listcollection)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
