---
title: RevisionCollection.RejectAll
linktitle: RejectAll
articleTitle: RejectAll
second_title: Aspose.Words для .NET
description: Откройте для себя метод RevisionCollection RejectAll, позволяющий легко отменять все изменения, оптимизируя рабочий процесс и улучшая управление документами.
type: docs
weight: 80
url: /ru/net/aspose.words/revisioncollection/rejectall/
---
## RevisionCollection.RejectAll method

Отклоняет все изменения в этой коллекции.

```csharp
public void RejectAll()
```

## Примеры

Показывает, как работать с коллекцией редакций документа.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Эта коллекция сама по себе содержит коллекцию групп ревизий.
// Каждая группа представляет собой последовательность смежных ревизий.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Проходим по коллекции групп и печатаем текст, к которому относится изменение.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Каждый запуск, на который влияет ревизия, получает соответствующий объект Revision.
// Коллекция изменений значительно больше, чем сжатая форма, которую мы напечатали выше,
// в зависимости от того, на сколько этапов мы сегментировали документ во время редактирования в Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange влияет строго на стили, а не на узлы документа. Это означает, что "ParentStyle"
        // свойство всегда будет использоваться, в то время как ParentNode всегда будет иметь значение null.
        // Поскольку все остальные изменения влияют на узлы, ParentNode, наоборот, будет использоваться, а ParentStyle будет иметь значение null.
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

// Отклонить все изменения через коллекцию, вернув документ к исходному виду.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Смотрите также

* class [RevisionCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
