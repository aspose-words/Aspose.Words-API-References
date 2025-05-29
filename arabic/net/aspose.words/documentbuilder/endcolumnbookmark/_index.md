---
title: DocumentBuilder.EndColumnBookmark
linktitle: EndColumnBookmark
articleTitle: EndColumnBookmark
second_title: Aspose.Words لـ .NET
description: استخدم طريقة EndColumnBookmark في DocumentBuilder لتمييز نهاية عمود في مستندك بسهولة. حسّن إدارة الجداول بدقة!
type: docs
weight: 220
url: /ar/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

يُحدِّد الموضع الحالي في المستند كعلامة مرجعية لنهاية العمود. يجب أن يكون الموضع في خلية جدول.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية. |

### قيمة الإرجاع

عقدة نهاية الإشارة المرجعية التي تم إنشاؤها للتو.

## ملاحظات

تغطي إشارة مرجعية العمود عمودًا واحدًا أو أكثر ضمن نطاق من الصفوف. لإنشاء إشارة مرجعية صالحة، عليك استدعاء كليهما.[`StartColumnBookmark`](../startcolumnbookmark/) و`EndColumnBookmark` مع نفس *bookmarkName* المعلمة.

سيتم تجاهل الإشارات المرجعية ذات التكوين السيئ أو الإشارات المرجعية التي تحتوي على أسماء مكررة عند حفظ المستند.

الموضع الفعلي للعنصر المُدرج[`BookmarkEnd`](../../bookmarkend/) قد تختلف العقدة عن موضع المنشئ document الحالي.

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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
