---
title: ListCollection
second_title: Справочник по API Aspose.Words для .NET
description: Хранит и управляет форматированием маркированных и нумерованных списков используемых в документе.
type: docs
weight: 3220
url: /ru/net/aspose.words.lists/listcollection/
---
## ListCollection class

Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе.

```csharp
public class ListCollection : IEnumerable<List>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count) { get; } | Получает количество нумерованных и маркированных списков в документе. |
| [Document](../../aspose.words.lists/listcollection/document) { get; } | Получает документ владельца. |
| [Item](../../aspose.words.lists/listcollection/item) { get; } | Получает список по индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add#add)(ListTemplate) | Создает новый список на основе предопределенного шаблона и добавляет его в коллекцию списков в документе. |
| [Add](../../aspose.words.lists/listcollection/add#add_1)(Style) | Создает новый список, ссылающийся на стиль списка, и добавляет его в коллекцию списков в документе. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy)(List) | Создает новый список, копируя указанный список и добавляя его к коллекции списков в документе. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator)() | Получает объект перечислителя, который будет перечислять списки в документе. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid)(int) | Получает список по идентификатору списка. |

### Примечания

Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Форматирование списков хранится в коллекции[`ListCollection`](../listcollection)отдельно от абзацев текста.

Вы не создаете объекты этого класса. Всегда существует только один[`ListCollection`](../listcollection) объект для каждого документа, и он доступен черезDocumentBaseсвойство.

Чтобы создать новый список на основе предопределенного шаблона списка или на основе стиля списка, используйте команду[`Add`](./add)метод.

Чтобы создать новый список с форматированием, идентичным существующему, используйте[`AddCopy`](./addcopy)метод.

Чтобы сделать абзац маркированным или пронумерованным, необходимо применить форматирование списка к абзацу, назначив[`List`](../list)объект [`List`](../listformat/list)свойствоФорматСписка.

Чтобы удалить форматирование списка из абзаца, используйте команду[`RemoveNumbers`](../listformat/removenumbers) метод.

Если вы немного знакомы с WordprocessingML, то, возможно, знаете, что он определяет отдельные понятия для "списка" и "определения списка". Это в точности соответствует тому, как сохраняется форматирование списка в документе Microsoft Word на низком уровне. Определение списка похоже на "схему", а list - на экземпляр определения списка.

Чтобы упростить модель программирования, Aspose.Words скрывает различие между определением list и list во многом так же, как Microsoft Word скрывает это в его пользовательский интерфейс. Это позволяет вам больше сосредоточиться на том, как должен выглядеть ваш документ, а не на создании низкоуровневых объектов для удовлетворения требований формата файла Microsoft Word.

В текущей версии Aspose.Words невозможно удалить списки после их создания. Это похоже на Microsoft Word, где пользователь не имеет явного контроля над определениями списков.

### Примеры

Показывает, как создать документ с образцом всех списков из другого документа.

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

* class [List](../list)
* пространство имен [Aspose.Words.Lists](../../aspose.words.lists)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
