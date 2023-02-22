---
title: Revision.ParentStyle
second_title: Справочник по API Aspose.Words для .NET
description: Revision свойство. Получает непосредственно родительский стиль владелец этой ревизии. Это свойство будет работать только дляStyleDefinitionChange тип ревизии.
type: docs
weight: 50
url: /ru/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Получает непосредственно родительский стиль (владелец) этой ревизии. Это свойство будет работать только дляStyleDefinitionChange тип ревизии.

```csharp
public Style ParentStyle { get; }
```

### Примечания

Если эта версия связана с изменениями в узлах документа, используйте[`ParentNode`](../parentnode/) вместо этого.

### Примеры

Показывает, как работать с набором редакций документа.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Сама эта коллекция имеет коллекцию групп ревизий.
// Каждая группа представляет собой последовательность смежных ревизий.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Перебираем набор групп и печатаем текст, к которому относится ревизия.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Каждый запуск, на который влияет ревизия, получает соответствующий объект ревизии.
// Коллекция ревизий значительно больше, чем сжатая форма, которую мы напечатали выше,
// в зависимости от того, на сколько прогонов мы сегментировали документ во время редактирования Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // StyleDefinitionChange строго влияет на стили, а не на узлы документа. Это означает "ParentStyle"
        // свойство всегда будет использоваться, а ParentNode всегда будет нулевым.
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

// Отклоняем все ревизии через коллекцию, возвращая документу его первоначальную форму.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Смотрите также

* class [Style](../../style/)
* class [Revision](../)
* пространство имен [Aspose.Words](../../revision/)
* сборка [Aspose.Words](../../../)


