---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words для .NET
description: Легко управляйте изменениями документов! Выбирайте между исходными или обновленными версиями для бесперебойной совместной работы и повышения производительности.
type: docs
weight: 380
url: /ru/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Возвращает или задает значение, указывающее, следует ли работать с исходной или измененной версией документа.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Примечания

Значение по умолчанию: .

## Примеры

Показывает, как переключаться между измененным и исходным видом документа.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Просмотр объекта документа, как будто все изменения приняты. В настоящее время поддерживает списочные метки.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Смотрите также

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
