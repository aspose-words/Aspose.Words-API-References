---
title: DocumentBuilder.EndColumnBookmark
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع في خلية الجدول.
type: docs
weight: 220
url: /ar/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية للعمود. يجب أن يكون الموضع في خلية الجدول.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية. |

### قيمة الإرجاع

عقدة نهاية الإشارة المرجعية التي تم إنشاؤها للتو.

### ملاحظات

تغطي الإشارة المرجعية للعمود عمودًا واحدًا أو أكثر في نطاق من الصفوف. لإنشاء إشارة مرجعية صالحة، يجب عليك الاتصال بكليهما[`StartColumnBookmark`](../startcolumnbookmark/) و`EndColumnBookmark` بنفس *bookmarkName*معامل.

سيتم تجاهل الإشارات المرجعية التي تم تكوينها بشكل سيئ أو الإشارات المرجعية ذات الأسماء المكررة عند حفظ المستند.

الموضع الفعلي للإدراج[`BookmarkEnd`](../../bookmarkend/) قد تختلف العقدة عن موضع منشئ document الحالي.

### أمثلة

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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


