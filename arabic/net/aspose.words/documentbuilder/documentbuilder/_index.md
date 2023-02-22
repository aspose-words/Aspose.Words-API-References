---
title: DocumentBuilder.DocumentBuilder
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder البناء. تهيئة مثيل جديد لهذه الفئة.
type: docs
weight: 10
url: /ar/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

تهيئة مثيل جديد لهذه الفئة.

```csharp
public DocumentBuilder()
```

### ملاحظات

ينشئ ملفًا جديدًا **DocumentBuilder** الكائن وإرفاقه بملف[`Document`](../document/) الكائن .

### أمثلة

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط ، ثم أضف نصًا.
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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## DocumentBuilder(Document) {#constructor_1}

تهيئة مثيل جديد لهذه الفئة.

```csharp
public DocumentBuilder(Document doc)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| doc | Document | كائن المستند المراد إرفاقه. |

### ملاحظات

ينشئ ملفًا جديدًا **DocumentBuilder** الكائن ، يعلق على المحدد[`Document`](../document/) object. تم وضع المؤشر في بداية المستند.

### أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوس وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// أنشئ الرؤوس ، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع رأس.
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

يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كمدخلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول محتويات للصفحة الأولى من المستند.
// تكوين الجدول لالتقاط فقرات بعناوين المستويات من 1 إلى 3.
// أيضًا ، قم بتعيين إدخالاتها لتكون ارتباطات تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الماوس الأيسر في Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// ملء جدول المحتويات بإضافة فقرات بأنماط عناوين.
// كل عنوان بمستوى بين 1 و 3 سينشئ إدخالاً في الجدول.
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

// جدول المحتويات هو حقل من النوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### أنظر أيضا

* class [Document](../../document/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


