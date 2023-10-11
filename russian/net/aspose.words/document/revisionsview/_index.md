---
title: Document.RevisionsView
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или задает значение указывающее следует ли работать с исходной или исправленной версией документа.
type: docs
weight: 360
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

Показывает, как переключаться между измененным и исходным видом документа.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Просматриваем объект документа так, как будто все изменения приняты. В настоящее время поддерживаются метки списков.
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


