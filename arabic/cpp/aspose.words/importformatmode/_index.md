---
title: "تعداد Aspose::Words::ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::ImportFormatMode. يحدد كيفية دمج التنسيق عند استيراد المحتوى من مستند آخر في C++."
type: docs
weight: 93000
url: /ar/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


يحدد كيفية دمج التنسيق عند استيراد المحتوى من مستند آخر.

```cpp
enum class ImportFormatMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| UseDestinationStyles | 0 | استخدم أنماط المستند الهدف ونسخ الأنماط الجديدة. هذا هو الخيار الافتراضي. |
| KeepSourceFormatting | 1 | انسخ جميع الأنماط المطلوبة إلى المستند الهدف، وأنشئ أسماء أنماط فريدة إذا لزم الأمر. |
| KeepDifferentStyles | 2 | انسخ الأنماط فقط إذا كانت مختلفة عن تلك الموجودة في المستند المصدر. |

## ملاحظات


عند نسخ العقد من مستند إلى آخر، يحدد هذا الخيار كيفية حل تنسيق الأنماط عندما يحتوي المستندان على نمط بنفس الاسم، لكن بتنسيق مختلف.

يتم حل التنسيق كما يلي:

1. يتم مطابقة الأنماط المدمجة باستخدام معرف النمط المستقل عن اللغة. يتم مطابقة الأنماط المعرفة من قبل المستخدم باستخدام اسم النمط حسّاس لحالة الأحرف.
1. إذا لم يتم العثور على نمط مطابق في المستند الهدف، يتم نسخ النمط (وجميع الأنماط المشار إليها) إلى المستند الهدف وتحديث العقد المستوردة للإشارة إلى النمط الجديد.
1. إذا كان هناك نمط مطابق موجود بالفعل في المستند الهدف، فإن ما يحدث يعتمد على المعامل **importFormatMode** الممرَّ إلى [ImportNode()](../) كما هو موضح أدناه.



عند استخدام خيار [UseDestinationStyles](./)، إذا كان هناك نمط مطابق موجود بالفعل في المستند الهدف، لا يتم نسخ النمط وتُحدَّث العقد المستوردة للإشارة إلى النمط الموجود.

العيب في استخدام [UseDestinationStyles](./) هو أن النص المستورد قد يبدو مختلفًا في المستند الهدف مقارنة بالمستند المصدر. على سبيل المثال، النمط \"Heading 1\" في المستند المصدر يستخدم خط Arial بحجم 16pt والنمط \"Heading 1\" في المستند الهدف يستخدم خط Times New Roman بحجم 14pt. عند استيراد نص النمط \"Heading 1\" دون أي تنسيق مباشر آخر، سيظهر بخط Times New Roman بحجم 14pt في المستند الهدف.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

العيب في استخدام [KeepSourceFormatting](./) هو أنه إذا قمت بإجراء عدة عمليات استيراد، قد ينتهي بك الأمر إلى وجود العديد من الأنماط في المستند الهدف، مما قد يجعل من الصعب استخدام تنسيق نمط متسق في Microsoft Word لهذا المستند.

يسمح خيار [KeepDifferentStyles](./) بإعادة استخدام أنماط الهدف إذا كان التنسيق الذي توفره مطابقًا للأنماط في المستند المصدر. إذا كان النمط في المستند الهدف مختلفًا عن المصدر، فسيتم استيراده.

## أمثلة



يوضح كيفية إدراج مستند داخل مستند آخر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
