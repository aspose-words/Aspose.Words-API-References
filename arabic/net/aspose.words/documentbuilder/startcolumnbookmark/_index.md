---
title: DocumentBuilder.StartColumnBookmark
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. تعليم الموضع الحالي في المستند كبداية إشارة عمود. يجب أن يكون الموضع في خلية جدول.
type: docs
weight: 590
url: /ar/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

تعليم الموضع الحالي في المستند كبداية إشارة عمود. يجب أن يكون الموضع في خلية جدول.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم المرجعية. |

### قيمة الإرجاع

عقدة بدء الإشارة المرجعية التي تم إنشاؤها للتو.

### ملاحظات

تغطي الإشارة المرجعية للعمود عمودًا واحدًا أو أكثر في نطاق من الصفوف. لإنشاء إشارة مرجعية صالحة you تحتاج إلى الاتصال بكليهما`StartColumnBookmark` و[`EndColumnBookmark`](../endcolumnbookmark/) بنفس_  **اسم العلامة** معامل.

سيتم تجاهل الإشارات المرجعية المكونة بشكل سيئ أو الإشارات المرجعية ذات الأسماء المكررة عند حفظ المستند.

الموضع الفعلي للادراج[`BookmarkStart`](../../bookmarkstart/) قد تختلف العقدة عن وضع document builder الحالي.

### أمثلة

يوضح كيفية إنشاء إشارة مرجعية للعمود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// سيتم وضع إشارة مرجعية على الخلايا 1،2،4،5.
builder.StartColumnBookmark("MyBookmark_1");
// سيتم تجاهل الإشارات المرجعية المكونة بشكل سيئ أو الإشارات المرجعية ذات الأسماء المكررة عند حفظ المستند.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### أنظر أيضا

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


