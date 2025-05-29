---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words لـ .NET
description: تحكم في فواصل الصفحات باستخدام خاصية ForcePageBreaks في TxtSaveOptionsBase. اضمن سلاسة في التصدير وحافظ على تنسيق المستندات بسلاسة.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

يسمح بتحديد ما إذا كان ينبغي الحفاظ على فواصل الصفحات أثناء التصدير.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## ملاحظات

تؤثر الخاصية فقط على فواصل الصفحات التي يتم إدراجها صراحةً في المستند. لا تتعلق بفواصل الصفحات التي يقوم MS Word بإدراجها تلقائيًا في نهاية كل صفحة.

## أمثلة

يوضح كيفية تحديد ما إذا كان سيتم الحفاظ على فواصل الصفحات عند تصدير مستند إلى نص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى "حفظ" المستند
// طريقة لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// تحتوي كائنات "Document" في Aspose.Words على فواصل صفحات، تمامًا مثل مستندات Microsoft Word.
//تنسيقات الحفظ مثل ".txt" هي عبارة عن نص متواصل بدون فواصل للصفحات.
// قم بضبط خاصية "ForcePageBreaks" على "true" للحفاظ على جميع فواصل الصفحات في شكل أحرف '\f'.
// قم بتعيين خاصية "ForcePageBreaks" إلى "false" لتجاهل جميع فواصل الصفحات.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// إذا قمنا بتحميل مستند نص عادي مع فواصل الصفحات،
//سيستخدمها كائن "المستند" لتقسيم النص إلى صفحات.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### أنظر أيضا

* class [TxtSaveOptionsBase](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
