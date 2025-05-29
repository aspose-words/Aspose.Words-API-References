---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertTableOfContents في DocumentBuilder، من خلال إضافة جدول محتويات ديناميكي لتسهيل التنقل وتحسين التنظيم.
type: docs
weight: 500
url: /ar/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

يقوم بإدراج حقل TOC (جدول المحتويات) في المستند.

```csharp
public Field InsertTableOfContents(string switches)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| switches | String | يتم تبديل حقل TOC. |

## ملاحظات

تقوم هذه الطريقة بإدراج حقل TOC (جدول المحتويات) في المستند في الموضع الحالي.

يمكن إنشاء جدول محتويات في مستند وورد بطرق متعددة، وتنسيقه باستخدام خيارات متنوعة. يتم التحكم في طريقة إنشاء الجدول وعرضه في وورد بواسطة مفاتيح الحقول.

أسهل طريقة لتحديد المفاتيح هي إدراج جدول محتويات x000d_ وتكوينه في مستند وورد باستخدام قائمة إدراج ← مرجع ← فهرس وجداول، ثم تشغيل عرض رموز الحقول لرؤية المفاتيح. يمكنك الضغط على Alt+F9 في Microsoft Word لتشغيل أو إيقاف عرض رموز الحقول.

على سبيل المثال، بعد إنشاء جدول المحتويات، يتم إدراج الحقل التالي في المستند:**{ جدول المحتويات \o "1-3" \h \z \u }** . يمكنك النسخ**\o "1-3" \h \z \u** واستخدامها كمعلمة للتبديل.

لاحظ أن`InsertTableOfContents` سيُدرج حقل جدول المحتويات فقط، لكن الأمر لن يُنشئ جدول المحتويات فعليًا. يُنشأ جدول المحتويات بواسطة Microsoft Word عند تحديث الحقل.

إذا قمت بإدراج جدول محتويات باستخدام هذه الطريقة ثم فتحت الملف في Microsoft Word، فلن تتمكن من رؤية جدول المحتويات لأن حقل جدول المحتويات لم يتم تحديثه بعد.

في Microsoft Word، لا يتم تحديث الحقول تلقائيًا عند فتح المستند، ولكن يمكنك تحديث الحقول في المستند في أي وقت عن طريق الضغط على F9.

## أمثلة

يوضح كيفية إدراج جدول المحتويات (TOC) في مستند باستخدام أنماط العناوين كإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج جدول المحتويات للصفحة الأولى من المستند.
// قم بتكوين الجدول لالتقاط الفقرات التي تحتوي على عناوين من المستويات 1 إلى 3.
// أيضًا، قم بتعيين إدخالاتها لتكون روابط تشعبية تأخذنا
// إلى موقع العنوان عند النقر بزر الماوس الأيسر في Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// قم بملء جدول المحتويات عن طريق إضافة فقرات ذات أنماط عناوين.
// كل عنوان من هذا القبيل بمستوى بين 1 و3 سوف ينشئ إدخالاً في الجدول.
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

// جدول المحتويات هو حقل من نوع يحتاج إلى التحديث لإظهار نتيجة محدثة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### أنظر أيضا

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
