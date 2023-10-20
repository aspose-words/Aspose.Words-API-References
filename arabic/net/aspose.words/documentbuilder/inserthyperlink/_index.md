---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words لـ .NET
description: DocumentBuilder InsertHyperlink طريقة. إدراج ارتباط تشعبي في المستند في C#.
type: docs
weight: 360
url: /ar/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

إدراج ارتباط تشعبي في المستند.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| displayText | String | نص الرابط الذي سيتم عرضه في الوثيقة. |
| urlOrBookmark | String | وجهة الارتباط. يمكن أن يكون عنوان url أو اسم إشارة مرجعية داخل المستند. تضيف هذه الطريقة دائمًا الفواصل العليا في بداية ونهاية عنوان url. |
| isBookmark | Boolean | `حقيقي` إذا كانت المعلمة السابقة عبارة عن اسم إشارة مرجعية داخل المستند؛ `خطأ شنيع` المعلمة السابقة هي عنوان URL. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) كائن يمثل الحقل المدرج.

## ملاحظات

لاحظ أنك تحتاج إلى تحديد تنسيق الخط لنص عرض الارتباط التشعبي صريح باستخدام ملف[`Font`](../font/) ملكية.

هذه الأساليب تدعو داخليا[`InsertField`](../insertfield/) لإدراج حقل MS Word HYPERLINK field في المستند.

## أمثلة

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

يوضح كيفية إدراج حقل الارتباط التشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// أدخل ارتباطًا تشعبيًا وقم بإبرازه بتنسيق مخصص.
// سيكون الارتباط التشعبي عبارة عن جزء من النص قابل للنقر عليه والذي سينقلنا إلى الموقع المحدد في عنوان URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com"، خطأ);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + النقر بزر الماوس الأيسر على الرابط الموجود في النص في Microsoft Word سينقلنا إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

يوضح كيفية استخدام مكدس التنسيق الخاص بمنشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإعداد تنسيق الخط، ثم اكتب النص الذي يسبق الارتباط التشعبي.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// الحفاظ على تكوين التنسيق الحالي لدينا على المكدس.
builder.PushFont();

// قم بتغيير التنسيق الحالي للمنشئ من خلال تطبيق نمط جديد.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com"، خطأ);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// استعادة تنسيق الخط الذي حفظناه سابقًا وإزالة العنصر من المكدس.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
