---
title: Paragraph.BreakIsStyleSeparator
linktitle: BreakIsStyleSeparator
articleTitle: BreakIsStyleSeparator
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية Paragraph Break IsStyleSeparator على تحسين تنسيق المستند من خلال السماح بأنماط فقرة مختلطة لتحقيق مرونة أكبر في التصميم.
type: docs
weight: 20
url: /ar/net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

صحيح إذا كان فاصل الفقرة هذا فاصل أنماط. يسمح فاصل الأنماط للفقرة الواحدة بأن تتكون من أجزاء ذات أنماط فقرات مختلفة.

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

// قم بإدراج فقرة بأسلوب سوف يلتقطه جدول المحتويات كإدخال.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// توجد كلتا السلسلتين في نفس الفقرة وبالتالي ستظهران في نفس إدخال جدول المحتويات.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// إذا قمنا بإدراج فاصل نمط، يمكننا كتابة المزيد من النص في نفس الفقرة
// واستخدم أسلوبًا مختلفًا دون أن يظهر في جدول المحتويات.
// إذا استخدمنا نمط نوع العنوان بعد الفاصل، فيمكننا رسم إدخالات جدول محتويات متعددة من سطر نص مستند واحد.
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
