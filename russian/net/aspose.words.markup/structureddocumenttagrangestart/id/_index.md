---
title: StructuredDocumentTagRangeStart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StructuredDocumentTagRangeStart Id — ваш ключ к уникальному числовому идентификатору, доступному только для чтения, для эффективной маркировки документов.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Указывает уникальный постоянный числовой идентификатор, доступный только для чтения, для этого структурированного тега документа.

```csharp
public int Id { get; }
```

## Примечания

Атрибут id должен соответствовать следующим правилам:

* Документ должен сохранять структурированные идентификаторы тегов документа только в том случае, если клонируется весь document [`Clone`](../../../aspose.words/document/clone/).
* В течение[`ImportNode`](../../../aspose.words/documentbase/importnode/) Идентификатор будет сохранен, если импорт не вызовет конфликтов с другими идентификаторами тегов структурированного документа в целевом документе.
* Если несколько структурированных узлов тега документа указывают одно и то же десятичное числовое значение для атрибута Id, , то первый структурированный тег документа в документе должен сохранить этот исходный Id, , а все последующие структурированные узлы тега документа должны иметь новые идентификаторы, назначенные им при загрузке документа.
* Во время тега отдельного структурированного документаINodeCloningListener) Для клонированного структурированного узла тега документа будет сгенерирован новый уникальный идентификатор операции be .
* Если идентификатор не указан в исходном документе, то структурированный узел тега документа будет иметь новый уникальный идентификатор, назначенный ему при загрузке документа.

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
