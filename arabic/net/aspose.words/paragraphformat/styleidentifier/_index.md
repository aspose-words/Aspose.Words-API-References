---
title: ParagraphFormat.StyleIdentifier
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تعيين معرف النمط المحلي المستقل لنمط الفقرة المطبق على هذا التنسيق.
type: docs
weight: 350
url: /ar/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

الحصول على أو تعيين معرف النمط المحلي المستقل لنمط الفقرة المطبق على هذا التنسيق.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### أمثلة

يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول محتويات للصفحة الأولى من المستند.
// قم بتكوين الجدول لالتقاط الفقرات ذات العناوين من المستويات 1 إلى 3.
// أيضًا، قم بتعيين إدخالاته لتكون روابط تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الماوس الأيسر في Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// قم بملء جدول المحتويات عن طريق إضافة فقرات بأنماط العناوين.
// كل عنوان بمستوى يتراوح بين 1 و 3 سيُنشئ مُدخلاً في الجدول.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// جدول المحتويات هو حقل من النوع الذي يحتاج إلى التحديث لإظهار نتيجة محدثة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### أنظر أيضا

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


