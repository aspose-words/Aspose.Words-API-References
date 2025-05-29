---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: Aspose.Words لـ .NET
description: استخدم طريقة StartColumnBookmark في DocumentBuilder لوضع علامة على مواضع خلايا الجدول كإشارات مرجعية للأعمدة بسهولة، مما يعزز التنقل في المستندات وتنظيمها.
type: docs
weight: 660
url: /ar/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

يُحدد الموضع الحالي في المستند كبداية إشارة مرجعية للعمود. يجب أن يكون الموضع في خلية جدول.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية. |

### قيمة الإرجاع

عقدة بدء الإشارة المرجعية التي تم إنشاؤها للتو.

## ملاحظات

تغطي إشارة مرجعية العمود عمودًا واحدًا أو أكثر ضمن نطاق من الصفوف. لإنشاء إشارة مرجعية صالحة، عليك استدعاء كليهما.`StartColumnBookmark` و[`EndColumnBookmark`](../endcolumnbookmark/) مع نفس *bookmarkName* المعلمة.

سيتم تجاهل الإشارات المرجعية ذات التكوين السيئ أو الإشارات المرجعية التي تحتوي على أسماء مكررة عند حفظ المستند.

الموضع الفعلي للعنصر المُدرج[`BookmarkStart`](../../bookmarkstart/) قد تختلف العقدة عن موضع المنشئ document الحالي.

## أمثلة

يوضح كيفية إنشاء إشارة مرجعية للعمود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// سيتم وضع إشارة مرجعية على الخلايا 1،2،4،5.
builder.StartColumnBookmark("MyBookmark_1");
// سيتم تجاهل الإشارات المرجعية ذات التكوين السيئ أو الإشارات المرجعية التي تحتوي على أسماء مكررة عند حفظ المستند.
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
