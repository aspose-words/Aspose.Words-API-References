---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: Aspose.Words لـ .NET
description: قم بوضع علامة على نهاية الإشارة المرجعية في مستندك بسهولة باستخدام طريقة EndBookmark في DocumentBuilder، مما يعمل على تحسين تنظيم مستندك وتنقله.
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

يمكن أن تتداخل الإشارات المرجعية في مستند ما وتمتد إلى أي نطاق. لإنشاء إشارة مرجعية صالحة، يجب عليك استدعاء كلٍّ من[`StartBookmark`](../startbookmark/) و`EndBookmark` مع نفس الشيء*bookmarkName* المعلمة .

سيتم تجاهل الإشارات المرجعية ذات التكوين السيئ أو الإشارات المرجعية التي تحتوي على أسماء مكررة عند حفظ المستند.

## أمثلة

يوضح كيفية إنشاء إشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يجب أن تحتوي الإشارة المرجعية الصالحة على نص مستند مُحاط بـ
// تم إنشاء عقد BookmarkStart وBookmarkEnd باسم إشارة مرجعية مطابق.
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

// أدخل حقل ارتباط تشعبي (HYPERLINK) يربط بالإشارة المرجعية. يمكننا تمرير مفاتيح الحقول
// إلى طريقة "InsertHyperlink" كجزء من الوسيطة التي تحتوي على اسم الإشارة المرجعية.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### أنظر أيضا

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
