---
title: List
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает список членом которого является данный абзац.
type: docs
weight: 20
url: /ru/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Получает или задает список, членом которого является данный абзац.

```csharp
public List List { get; set; }
```

### Примечания

Список, который назначается этому свойству, должен принадлежать текущему документу.

Список, назначаемый этому свойству, не должен быть определением стиля списка.

Установка для этого свойства значения null удаляет маркеры и нумерацию из абзаца и устанавливает нулевой номер уровня списка. Установка для этого свойства значения null эквивалентна вызову[`RemoveNumbers`](../removenumbers).

### Примеры

Показывает, как вложить список в другой список.

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
* class [ListFormat](../../listformat)
* namespace [Aspose.Words.Lists](../../listformat)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
