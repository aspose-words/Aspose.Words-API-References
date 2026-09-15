---
title: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode"
linktitle: "get_ListExportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode. يحدد كيفية كتابة عناصر القائمة إلى ملف الإخراج. القيمة الافتراضية هي MarkdownSyntax في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


يحدد كيفية كتابة عناصر القائمة إلى ملف الإخراج. القيمة الافتراضية هي [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## ملاحظات


عند ضبط هذه الخاصية على [PlainText](../../markdownlistexportmode/) يتم تحديث جميع تسميات القائمة باستخدام [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) وتصديرها بالقيم الفعلية لها. قد تكون مثل هذه القوائم غير متوافقة مع تنسيق Markdown وسيتم التعرف عليها كنص عادي عند الاستيراد في هذه الحالة.

عند ضبط هذه الخاصية على [MarkdownSyntax](../../markdownlistexportmode/)، يحاول الكاتب تصدير عناصر القائمة بطريقة تسمح بترقيم العناصر تلقائيًا باستخدام Markdown.

## أمثلة



يظهر كيف سيتم كتابة عناصر القائمة إلى مستند markdown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// استخدم MarkdownListExportMode.PlainText أو MarkdownListExportMode.MarkdownSyntax لتصدير القائمة.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## انظر أيضًا

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
