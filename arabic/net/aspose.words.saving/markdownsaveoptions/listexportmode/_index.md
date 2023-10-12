---
title: MarkdownSaveOptions.ListExportMode
second_title: Aspose.Words لمراجع .NET API
description: MarkdownSaveOptions ملكية. يحدد كيفية كتابة عناصر القائمة في ملف الإخراج. القيمة الافتراضية هيMarkdownSyntax .
type: docs
weight: 60
url: /ar/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

يحدد كيفية كتابة عناصر القائمة في ملف الإخراج. القيمة الافتراضية هيMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

### ملاحظات

عندما يتم تعيين هذه الخاصية إلىPlainText يتم تحديث كافة تسميات القائمة باستخدام[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/)وتصديرها بقيمتها الفعلية. يمكن أن تكون هذه القوائم غير متوافقة مع تنسيق Markdown وسيتم التعرف عليها كنص عادي عند الاستيراد في هذه الحالة.

عندما يتم تعيين هذه الخاصية إلىMarkdownSyntaxيحاول الكاتب تصدير عناصر القائمة إلى x000d بطريقة تسمح بترقيم عناصر القائمة في الوضع التلقائي بواسطة Markdown.

### أمثلة

يوضح كيفية إدراج العناصر التي سيتم كتابتها في مستند تخفيض السعر.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// استخدم MarkdownListExportMode.PlainText أو MarkdownListExportMode.MarkdownSyntax لتصدير القائمة.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### أنظر أيضا

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../markdownsaveoptions/)
* المجسم [Aspose.Words](../../../)


