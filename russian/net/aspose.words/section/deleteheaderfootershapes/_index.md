---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: Aspose.Words для .NET
description: С легкостью удаляйте все фигуры из верхних и нижних колонтитулов разделов с помощью метода DeleteHeaderFooterShapes для более четкого представления документа.
type: docs
weight: 140
url: /ru/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Удаляет все фигуры (объекты рисования) из верхних и нижних колонтитулов этого раздела.

```csharp
public void DeleteHeaderFooterShapes()
```

## Примеры

Показывает, как удалить все фигуры из всех верхних и нижних колонтитулов в разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем основной заголовок с формой.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Создаем основной нижний колонтитул с изображением.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// Удалить все фигуры из верхних и нижних колонтитулов в первом разделе.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
