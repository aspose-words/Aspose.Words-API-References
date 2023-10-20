---
title: DocumentBase.Lists
linktitle: Lists
articleTitle: Lists
second_title: Aspose.Words для .NET
description: DocumentBase Lists свойство. Предоставляет доступ к форматированию списка используемому в документе на С#.
type: docs
weight: 40
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

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
