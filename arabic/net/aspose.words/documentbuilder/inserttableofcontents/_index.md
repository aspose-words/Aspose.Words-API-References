---
title: DocumentBuilder.InsertTableOfContents
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج حقل TOC جدول المحتويات في المستند.
type: docs
weight: 470
url: /ar/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

إدراج حقل TOC (جدول المحتويات) في المستند.

```csharp
public Field InsertTableOfContents(string switches)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| switches | String | يقوم حقل TOC بالتبديل. |

### ملاحظات

تقوم هذه الطريقة بإدراج حقل TOC (جدول المحتويات) في المستند عند الموضع الحالي.

يمكن إنشاء جدول محتويات في مستند Word بعدة طرق وتنسيقه باستخدام مجموعة متنوعة من الخيارات. يتم التحكم في طريقة إنشاء الجدول وعرضه بواسطة Microsoft Word بواسطة مفاتيح التبديل الميدانية.

أسهل طريقة لتحديد المفاتيح هي إدراج جدول محتويات وتكوينه في مستند Word باستخدام القائمة إدراج-&gt;مرجع-&gt;الفهرس والجداول، ثم تشغيل عرض رموز الحقول لرؤية المفاتيح. يمكنك الضغط على Alt+F9 in Microsoft Word للتبديل بين تشغيل أو إيقاف عرض رموز الحقول.

على سبيل المثال، بعد إنشاء جدول المحتويات، يتم إدراج الحقل التالي في المستند: **{ جدول المحتويات \o "1-3" \h \z \u }** . يمكنك النسخ **\o "1-3" \h \z \u** واستخدامها كمعلمة التبديل.

لاحظ أن`InsertTableOfContents` سيقوم فقط بإدراج حقل جدول المحتويات، لكن لن يقوم فعليًا بإنشاء جدول المحتويات. تم إنشاء جدول المحتويات بواسطة Microsoft Word عند تحديث الحقل.

إذا قمت بإدراج جدول محتويات باستخدام هذه الطريقة ثم قمت بفتح file في Microsoft Word، فلن ترى جدول المحتويات لأن جدول المحتويات field لم يتم تحديثه بعد.

في Microsoft Word، لا يتم تحديث الحقول تلقائيًا عند فتح مستند، ولكن يمكنك تحديث الحقول في مستند في أي وقت بالضغط على F9.

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

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


