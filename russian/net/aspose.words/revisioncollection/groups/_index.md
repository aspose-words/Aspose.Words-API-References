---
title: RevisionCollection.Groups
second_title: Справочник по API Aspose.Words для .NET
description: RevisionCollection свойство. Коллекция групп редакций.
type: docs
weight: 20
url: /ru/net/aspose.words/revisioncollection/groups/
---
## RevisionCollection.Groups property

Коллекция групп редакций.

```csharp
public RevisionGroupCollection Groups { get; }
```

### Примеры

Показывает, как работать с коллекцией редакций документа.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Эта коллекция сама содержит набор групп ревизий.
// Каждая группа представляет собой последовательность соседних ревизий.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Перебираем коллекцию групп и печатаем текст, к которому относится редакция.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Каждый запуск, на который влияет ревизия, получает соответствующий объект ревизии.
// Коллекция редакций значительно больше, чем в сокращенной форме, которую мы напечатали выше,
// в зависимости от того, на сколько прогонов мы сегментировали документ во время редактирования Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange влияет исключительно на стили, а не на узлы документа. Это означает «Родительский стиль».
        // Свойство всегда будет использоваться, а ParentNode всегда будет иметь значение null.
        // Поскольку все остальные изменения затрагивают узлы, ParentNode, наоборот, будет использоваться, а ParentStyle будет иметь значение null.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Отклоняем все изменения через коллекцию, возвращая документ в исходную форму.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Смотрите также

* class [RevisionGroupCollection](../../revisiongroupcollection/)
* class [RevisionCollection](../)
* пространство имен [Aspose.Words](../../revisioncollection/)
* сборка [Aspose.Words](../../../)


