---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك باستخدام طريقة InsertHyperlink في DocumentBuilder، وقم بإضافة روابط قابلة للنقر بسهولة لتحسين التنقل وإشراك المستخدم.
type: docs
weight: 390
url: /ar/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

إدراج ارتباط تشعبي في المستند.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| displayText | String | نص الرابط الذي سيتم عرضه في المستند. |
| urlOrBookmark | String | وجهة الرابط. يمكن أن يكون عنوان URL أو اسم إشارة مرجعية داخل المستند. تُضيف هذه الطريقة دائمًا علامات اقتباس في بداية ونهاية عنوان URL. |
| isBookmark | Boolean | `حقيقي` إذا كانت المعلمة السابقة عبارة عن اسم إشارة مرجعية داخل المستند؛ `خطأ شنيع` المعلمة السابقة هي عنوان URL. |

### قيمة الإرجاع

أ[`Field`](../../../aspose.words.fields/field/) الكائن الذي يمثل الحقل المدرج.

## ملاحظات

لاحظ أنك تحتاج إلى تحديد تنسيق الخط لنص عرض الارتباط التشعبي صراحةً باستخدام[`Font`](../font/) ملكية.

هذه الأساليب تدعو داخليًا[`InsertField`](../insertfield/)لإدراج حقل الارتباط التشعبي MS Word في المستند.

## أمثلة

يوضح كيفية إدراج حقل ارتباط تشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

//أدرج ارتباطًا تشعبيًا وأبرزه باستخدام التنسيق المخصص.
// سيكون الرابط التشعبي عبارة عن جزء نصي قابل للنقر والذي سيأخذنا إلى الموقع المحدد في عنوان URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com"، خطأ);
builder.Font.ClearFormatting();
builder.Writeln(".");

// الضغط على Ctrl + النقر بزر الماوس الأيسر على الرابط الموجود في النص في Microsoft Word سيأخذنا إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
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

يوضح كيفية استخدام مجموعة التنسيق الخاصة بمنشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإعداد تنسيق الخط، ثم اكتب النص الذي يسبق الارتباط التشعبي.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

//الحفاظ على تكوين التنسيق الحالي على المكدس.
builder.PushFont();

// تغيير تنسيق المنشئ الحالي من خلال تطبيق نمط جديد.
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
