---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words لـ .NET
description: DocumentBuilder StartColumnBookmark طريقة. يحدد الموضع الحالي في المستند كبداية عمود الإشارة المرجعية. يجب أن يكون الموضع في خلية الجدول في C#.
type: docs
weight: 620
url: /ar/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

يحدد الموضع الحالي في المستند كبداية عمود الإشارة المرجعية. يجب أن يكون الموضع في خلية الجدول.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية. |

### قيمة الإرجاع

عقدة بداية الإشارة المرجعية التي تم إنشاؤها للتو.

## ملاحظات

تغطي الإشارة المرجعية للعمود عمودًا واحدًا أو أكثر في نطاق من الصفوف. لإنشاء إشارة مرجعية صالحة، يجب عليك الاتصال بكليهما`StartColumnBookmark` و[`EndColumnBookmark`](../endcolumnbookmark/) بنفس *bookmarkName*معامل.

سيتم تجاهل الإشارات المرجعية التي تم تكوينها بشكل سيئ أو الإشارات المرجعية ذات الأسماء المكررة عند حفظ المستند.

الموضع الفعلي للإدراج[`BookmarkStart`](../../bookmarkstart/) قد تختلف العقدة عن موضع منشئ document الحالي.

## أمثلة

يوضح كيفية إنشاء إشارة مرجعية للعمود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// سيتم وضع إشارة مرجعية على الخلايا 1،2،4،5.
builder.StartColumnBookmark("MyBookmark_1");
// سيتم تجاهل الإشارات المرجعية التي تم تشكيلها بشكل سيئ أو الإشارات المرجعية ذات الأسماء المكررة عند حفظ المستند.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
