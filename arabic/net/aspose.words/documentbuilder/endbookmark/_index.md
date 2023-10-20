---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words لـ .NET
description: DocumentBuilder EndBookmark طريقة. يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية في C#.
type: docs
weight: 210
url: /ar/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

يحدد الموضع الحالي في المستند كنهاية إشارة مرجعية.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | اسم الإشارة المرجعية. |

### قيمة الإرجاع

عقدة نهاية الإشارة المرجعية التي تم إنشاؤها للتو.

## ملاحظات

يمكن أن تتداخل الإشارات المرجعية الموجودة في المستند وتمتد إلى أي نطاق. لإنشاء إشارة مرجعية صالحة تحتاج إلى استدعاء كليهما[`StartBookmark`](../startbookmark/) و`EndBookmark` مع نفس الشيء*bookmarkName* المعلمة.

سيتم تجاهل الإشارات المرجعية التي تم تكوينها بشكل سيئ أو الإشارات المرجعية ذات الأسماء المكررة عند حفظ المستند.

## أمثلة

يوضح كيفية إنشاء إشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الإشارة المرجعية الصالحة تحتاج إلى أن يكون النص الأساسي للمستند محاطًا بها
// عُقد BookmarkStart وBookmarkEnd التي تم إنشاؤها باستخدام اسم إشارة مرجعية مطابق.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

يوضح كيفية إدراج ارتباط تشعبي يشير إلى إشارة مرجعية محلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// أدخل حقل الارتباط التشعبي الذي يرتبط بالإشارة المرجعية. يمكننا تمرير مفاتيح المجال
// إلى أسلوب "InsertHyperlink" كجزء من الوسيطة التي تحتوي على اسم الإشارة المرجعية.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### أنظر أيضا

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
