---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words для .NET
description: StructuredDocumentTagRangeStart Id свойство. Указывает уникальный постоянный числовой идентификатор доступный только для чтения для этого тега структурированного документа на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Указывает уникальный постоянный числовой идентификатор, доступный только для чтения, для этого тега структурированного документа.

```csharp
public int Id { get; }
```

## Примечания

Атрибут Id должен соответствовать следующим правилам:

* Документ должен сохранять идентификаторы тегов структурированного документа только в том случае, если весь document клонирован.[`Clone`](../../../aspose.words/document/clone/).
* В течение[`ImportNode`](../../../aspose.words/documentbase/importnode/) Идентификатор должен быть сохранен, если импорт не вызывает конфликтов с другими идентификаторами тегов структурированного документа в целевого документа.
* Если несколько узлов тега структурированного документа указывают одно и то же значение десятичного числа для атрибута Id, , тогда первый тег структурированного документа в документе должен поддерживать этот исходный идентификатор, , а всем последующим узлам тега структурированного документа должны быть присвоены новые идентификаторы, когда документ загружен.
* Во время тега автономного структурированного документаINodeCloningListener)для узла тега клонированного структурированного документа будет сгенерирован новый уникальный идентификатор .
* Если идентификатор не указан в исходном документе, то узлу тега структурированного документа должен быть присвоен новый уникальный идентификатор при загрузке документа.

## Примеры

Показывает, как получить свойства тегов многосекционного структурированного документа.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Смотрите также

* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
