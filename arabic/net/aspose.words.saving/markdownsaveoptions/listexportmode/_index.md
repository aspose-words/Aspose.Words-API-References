---
title: MarkdownSaveOptions.ListExportMode
linktitle: ListExportMode
articleTitle: ListExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ListExportMode في MarkdownSaveOptions، التي تتحكم في كيفية إخراج عناصر القائمة. حسّن ملفاتك باستخدام MarkdownSyntax المرن!
type: docs
weight: 110
url: /ar/net/aspose.words.saving/markdownsaveoptions/listexportmode/
---
## MarkdownSaveOptions.ListExportMode property

يحدد كيفية كتابة عناصر القائمة إلى ملف الإخراج. القيمة الافتراضية هيMarkdownSyntax .

```csharp
public MarkdownListExportMode ListExportMode { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية علىPlainText يتم تحديث جميع تسميات القائمة باستخدام[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) ويتم تصديرها بقيمها الفعلية. قد لا تكون هذه القوائم متوافقة مع تنسيق Markdown، وسيتم التعرف عليها كنص عادي عند استيرادها في هذه الحالة.

عندما يتم تعيين هذه الخاصية علىMarkdownSyntaxيحاول الكاتب تصدير عناصر القائمة x000d_ بطريقة تسمح بترقيم عناصر القائمة في الوضع التلقائي بواسطة Markdown.

## أمثلة

يوضح كيفية إدراج العناصر التي سيتم كتابتها في مستند Markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// استخدم MarkdownListExportMode.PlainText أو MarkdownListExportMode.MarkdownSyntax لتصدير القائمة.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### أنظر أيضا

* enum [MarkdownListExportMode](../../markdownlistexportmode/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
