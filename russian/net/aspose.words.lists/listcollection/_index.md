---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.Lists.ListCollection сорт. Хранит и управляет форматированием маркированных и нумерованных списков используемых в документе на С#.
type: docs
weight: 3470
url: /ru/net/aspose.words.lists/listcollection/
---
## ListCollection class

Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе.

Чтобы узнать больше, посетите[Работа со списками](https://docs.aspose.com/words/net/working-with-lists/) статья документации.

```csharp
public class ListCollection : IEnumerable<List>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Получает количество нумерованных и маркированных списков в документе. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Получает документ владельца. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Получает список по индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | Создает новый список на основе предопределенного шаблона и добавляет его в коллекцию списков в документе. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | Создает новый список, ссылающийся на стиль списка, и добавляет его в коллекцию списков в документе. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | Создает новый список, копируя указанный список и добавляя его в коллекцию списков в документе. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Получает объект перечислителя, который будет перечислять списки в документе. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | Получает список по идентификатору списка. |

## Примечания

Список в документе Microsoft Word представляет собой набор свойств форматирования списка. Форматирование списков хранится в`ListCollection` сбор отдельно из абзацев текста.

Вы не создаете объекты этого класса. Всегда есть только один`ListCollection` для каждого документа и доступен через[`Lists`](../../aspose.words/documentbase/lists/) свойство.

Чтобы создать новый список на основе предопределенного шаблона списка или на основе стиля списка, используйте команду[`Add`](./add/) метод.

Чтобы создать новый список с форматированием, идентичным существующему списку, используйте команду[`AddCopy`](./addcopy/) метод.

Чтобы сделать абзац маркированным или нумерованным, вам необходимо применить к абзацу list formatting , присвоив ему[`List`](../list/)возражать против the [`List`](../listformat/list/) свойство[`ListFormat`](../listformat/).

Чтобы удалить форматирование списка из абзаца, используйте команду[`RemoveNumbers`](../listformat/removenumbers/) метод.

Если вы немного знакомы с WordprocessingML, то, возможно, знаете, что он определяет отдельные Concept для «списка» и «определения списка». Это в точности соответствует тому, как форматирование списка хранится в документе Microsoft Word на нижнем уровне. Определение списка похоже на «схему», а список — на экземпляр определения списка.

Чтобы упростить модель программирования, Aspose.Words скрывает различие между определением list и list почти так же, как Microsoft Word скрывает это в своем пользовательском интерфейсе. Это позволяет вам больше сосредоточиться на том, как вы хотите, чтобы ваш документ выглядел, а не на создание объектов низкого уровня для удовлетворения требований формата файлов Microsoft Word.

Невозможно удалить списки после их создания в текущей версии Aspose.Words. . Это похоже на Microsoft Word, где пользователь не имеет явного контроля над определениями списков.

## Примеры

Показывает, как создать документ с выборкой всех списков из другого документа.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

Показывает, как возобновить нумерацию в списке путем копирования списка.

```csharp
Document doc = new Document();

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
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

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев путем нумерации каждого элемента.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство ListLevelNumber, мы можем повысить уровень списка
// чтобы начать автономный подсписок с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
 // На более глубоких уровнях списка используются буквы и строчные римские цифры.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// Этот список будет применять отступ и символ маркера («•») перед каждым абзацем.
// На более глубоких уровнях этого списка будут использоваться другие символы, например «■» и «○».
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

* class [List](../list/)
* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
