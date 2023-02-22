---
title: Document.RevisionsView
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или задает значение указывающее следует ли работать с исходной или исправленной версией документа.
type: docs
weight: 340
url: /ru/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Получает или задает значение, указывающее, следует ли работать с исходной или исправленной версией документа.

```csharp
public RevisionsView RevisionsView { get; set; }
```

### Примечания

Значение по умолчанию: .

### Примеры

Показывает, как переключаться между исправленным и исходным видом документа.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Просмотр объекта документа, как если бы все изменения были приняты. В настоящее время поддерживает метки списка.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Смотрите также

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


