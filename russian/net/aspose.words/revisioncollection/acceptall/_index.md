---
title: AcceptAll
second_title: Справочник по API Aspose.Words для .NET
description: Принимает все версии в этой коллекции.
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

// Сравнение документов с ревизиями вызовет исключение.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// После сравнения исходный документ получит новую ревизию
// для каждого отличающегося элемента в редактируемом документе.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Принятие этих изменений преобразует исходный документ в отредактированный документ.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Смотрите также

* class [RevisionCollection](../../revisioncollection)
* пространство имен [Aspose.Words](../../revisioncollection)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->