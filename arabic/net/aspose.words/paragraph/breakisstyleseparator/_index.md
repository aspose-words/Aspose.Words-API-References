---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words لـ .NET
description: Paragraph BreakIsStyleSeparator ملكية. صحيح إذا كان فاصل الفقرة هذا عبارة عن فاصل نمط. يسمح فاصل الأنماط بأن تتكون فقرة one من أجزاء لها أنماط فقرات مختلفة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

صحيح إذا كان فاصل الفقرة هذا عبارة عن فاصل نمط. يسمح فاصل الأنماط بأن تتكون فقرة one من أجزاء لها أنماط فقرات مختلفة.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## أمثلة

يوضح كيفية كتابة نص في نفس السطر كعنوان جدول المحتويات وعدم ظهوره في جدول المحتويات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// أدخل فقرة بنمط سيختاره جدول المحتويات كمدخل.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// كلا السلسلتين موجودتان في نفس الفقرة وبالتالي ستظهران في نفس إدخال جدول المحتويات.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// إذا قمنا بإدراج فاصل نمط، فيمكننا كتابة المزيد من النص في نفس الفقرة
// واستخدم نمطًا مختلفًا دون الظهور في جدول المحتويات.
// إذا استخدمنا نمط نوع العنوان بعد الفاصل، فيمكننا رسم إدخالات جدول المحتويات المتعددة من سطر نص مستند واحد.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
