---
title: Section.DeleteHeaderFooterShapes
second_title: Справочник по API Aspose.Words для .NET
description: Section метод. Удаляет все фигуры объекты рисования из верхних и нижних колонтитулов этого раздела.
type: docs
weight: 120
url: /ru/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Удаляет все фигуры (объекты рисования) из верхних и нижних колонтитулов этого раздела.

```csharp
public void DeleteHeaderFooterShapes()
```

### Примеры

Показывает, как удалить все фигуры из всех заголовков и нижних колонтитулов в разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем основной заголовок с фигурой.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Создаем основной нижний колонтитул с изображением.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo Icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// Удаляем все фигуры из верхних и нижних колонтитулов в первом разделе.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


