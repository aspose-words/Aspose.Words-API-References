---
title: DocumentBase.Lists
linktitle: Lists
articleTitle: Lists
second_title: Aspose.Words для .NET
description: Откройте для себя DocumentBase Lists для эффективного управления имуществом. Получите доступ к настраиваемому форматированию списков, чтобы улучшить представление и ясность вашего документа.
type: docs
weight: 50
url: /ru/net/aspose.words/documentbase/lists/
---
## DocumentBase.Lists property

Предоставляет доступ к форматированию списка, используемому в документе.

```csharp
public ListCollection Lists { get; }
```

## Примечания

Более подробную информацию смотрите в описании[`ListCollection`](../../../aspose.words.lists/listcollection/) сорт.

## Примеры

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев путем нумерации каждого элемента.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство "ListLevelNumber", мы можем увеличить уровень списка
// для начала автономного подсписка с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
 // Более глубокие уровни списка используют буквы и строчные римские цифры.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// В этом списке перед каждым абзацем будет применен отступ и символ маркера ("•").
// Более глубокие уровни этого списка будут использовать другие символы, такие как «■» и «○».
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

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
