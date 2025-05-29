---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: Aspose.Words لـ .NET
description: قم بإزالة جميع أشكال الرسم بسهولة من رؤوس وتذييلات الأقسام باستخدام طريقة DeleteHeaderFooterShapes لتقديم عرض مستند أنظف.
type: docs
weight: 140
url: /ar/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

يحذف جميع الأشكال (كائنات الرسم) من رؤوس وتذييلات هذا القسم.

```csharp
public void DeleteHeaderFooterShapes()
```

## أمثلة

يوضح كيفية إزالة كافة الأشكال من كافة الرؤوس والتذييلات في القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء رأس رئيسي مع شكل.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// إنشاء تذييل أساسي مع صورة.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// قم بإزالة كافة الأشكال من الرؤوس والتذييلات في القسم الأول.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
