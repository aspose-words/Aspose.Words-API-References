---
title: StructuredDocumentTagRangeStart.Id
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTagRangeStart свойство. Указывает уникальный постоянный числовой идентификатор только для чтения для этого тега структурированного документа.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/id/
---
## StructuredDocumentTagRangeStart.Id property

Указывает уникальный постоянный числовой идентификатор только для чтения для этого тега структурированного документа.

```csharp
public int Id { get; }
```

### Примечания

Атрибут идентификатора должен соответствовать следующим правилам:

* Документ должен сохранять идентификаторы тегов структурированного документа, только если весь документ клонирован.[`Clone`](../../../aspose.words/document/clone/).
* В течение[`ImportNode`](../../../aspose.words/documentbase/importnode/) Идентификатор должен быть сохранен, если импорт не вызывает конфликтов с другими идентификаторами тегов структурированного документа в целевого документа.
* Если несколько узлов тегов структурированного документа задают одно и то же значение десятичного числа для атрибута Id, , то первый тег структурированного документа в документе должен поддерживать этот исходный идентификатор, , а все последующие узлы тегов структурированного документа должны иметь новые идентификаторы, назначенные им, когда документ загружен.
* Во время тега автономного структурированного документаINodeCloningListener) операции новый уникальный идентификатор будет сгенерирован для клонированного узла тега структурированного документа.
* Если Id не указан в исходном документе, то узел тега структурированного документа должен иметь новый уникальный идентификатор, присвоенный ему при загрузке документа.

### Примеры

Показывает, как получить свойства тегов структурированного документа, состоящего из нескольких разделов.

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
* пространство имен [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* сборка [Aspose.Words](../../../)


