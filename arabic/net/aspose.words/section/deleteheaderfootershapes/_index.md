---
title: Section.DeleteHeaderFooterShapes
second_title: Aspose.Words لمراجع .NET API
description: Section طريقة. حذف كافة الأشكال الكائنات الرسومية من رؤوس وتذييلات هذا القسم.
type: docs
weight: 140
url: /ar/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

حذف كافة الأشكال (الكائنات الرسومية) من رؤوس وتذييلات هذا القسم.

```csharp
public void DeleteHeaderFooterShapes()
```

### أمثلة

يوضح كيفية إزالة كافة الأشكال من كافة الرؤوس والتذييلات في القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أنشئ رأسًا أساسيًا بالشكل.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// قم بإنشاء تذييل أساسي مع صورة.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo Icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// قم بإزالة جميع الأشكال من الرؤوس والتذييلات في القسم الأول.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


