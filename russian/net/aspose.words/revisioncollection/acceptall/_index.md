---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words для .NET
description: Откройте для себя метод RevisionCollection AcceptAll для бесшовной интеграции всех изменений, повышения эффективности рабочего процесса и совместной работы.
type: docs
weight: 50
url: /ru/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Принимает все изменения в этой коллекции.

```csharp
public void AcceptAll()
```

## Примеры

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

// После сравнения исходный документ получит новую версию
// для каждого элемента, отличающегося в редактируемом документе.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Принятие этих изменений преобразует исходный документ в отредактированный документ.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Смотрите также

* class [RevisionCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
