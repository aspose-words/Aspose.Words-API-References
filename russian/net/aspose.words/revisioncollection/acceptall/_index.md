---
title: RevisionCollection.AcceptAll
second_title: Справочник по API Aspose.Words для .NET
description: RevisionCollection метод. Принимает все версии в этой коллекции.
type: docs
weight: 40
url: /ru/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Принимает все версии в этой коллекции.

```csharp
public void AcceptAll()
```

### Примеры

Показывает, как сравнивать документы.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Сравнение документов с редакциями вызовет исключение.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// После сравнения исходный документ получит новую редакцию
// для каждого элемента, отличающегося в редактируемом документе.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Принятие этих изменений приведет к преобразованию исходного документа в отредактированный документ.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Смотрите также

* class [RevisionCollection](../)
* пространство имен [Aspose.Words](../../revisioncollection/)
* сборка [Aspose.Words](../../../)


