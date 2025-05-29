---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: Aspose.Words لـ .NET
description: أنشئ مستندات قوية بكل سهولة مع DocumentBuilder. أنشئ نسخة جديدة وسهّل إدارة مستنداتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public DocumentBuilder()
```

## ملاحظات

ينشئ جديدًا[`DocumentBuilder`](../)الكائن ويربطه بجسم جديد[`Document`](../../document/) الكائن.

## أمثلة

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط، ثم أضف النص.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## ملاحظات

ينشئ جديدًا[`DocumentBuilder`](../)الكائن ويربطه بجسم جديد[`Document`](../../document/) object. يمكن تحديد خيارات إضافية لبناء المستندات.

## أمثلة

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

//يضيف المحتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
//تغيير حجم الخط داخل الجدول.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// إذا كان ContextTableFormatting صحيحًا، فلن يتم تطبيق تنسيق الجدول على المحتوى بعد ذلك.
// إذا كان ContextTableFormatting خاطئًا، فسيتم تطبيق تنسيق الجدول على المحتوى بعد ذلك.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### أنظر أيضا

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public DocumentBuilder(Document doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | Document | ال[`Document`](../../document/) كائن لربطه. |

## ملاحظات

ينشئ جديدًا[`DocumentBuilder`](../) الكائن، يرتبط بالشيء المحدد[`Document`](../../document/) الكائن. يقع المؤشر في بداية المستند.

## أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// قم بإنشاء الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من أنواع الرؤوس.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

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

* class [Document](../../document/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | Document | ال[`Document`](../../document/) كائن لربطه. |
| options | DocumentBuilderOptions | خيارات إضافية لعملية بناء المستندات. |

## ملاحظات

ينشئ جديدًا[`DocumentBuilder`](../) الكائن، يرتبط بالشيء المحدد[`Document`](../../document/) الكائن. يقع المؤشر في بداية المستند.

## أمثلة

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

//يضيف المحتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
//تغيير حجم الخط داخل الجدول.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// إذا كان ContextTableFormatting صحيحًا، فلن يتم تطبيق تنسيق الجدول على المحتوى بعد ذلك.
// إذا كان ContextTableFormatting خاطئًا، فسيتم تطبيق تنسيق الجدول على المحتوى بعد ذلك.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### أنظر أيضا

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
