---
title: "Aspose::Words::PageExtractOptions فئة"
linktitle: "PageExtractOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::PageExtractOptions. تسمح بتحديد الخيارات لاستخراج صفحات المستند في C++."
type: docs
weight: 45500
url: /ar/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


يسمح بتحديد خيارات استخراج صفحات المستند.

```cpp
class PageExtractOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | يحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. القيمة الافتراضية هي **true**. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | يحدد ما إذا كان رقم صفحة البداية في المستند الناتج سيُحدَّث. القيمة الافتراضية هي **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | دالة ضبط لـ [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | دالة ضبط لـ [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

## أمثلة



إظهار كيفية إعادة تعيين ترقيم الصفحات الأولي وحفظ حقل NUMPAGE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// السلوك الافتراضي:
// ترقيم الصفحات المستخرج هو نفسه كما في المستند الأصلي، كما لو أننا اخترنا "Print 2 pages" في MS Word.
// سيتم تعيين صفحة البداية إلى 2 وسيتم إزالة الحقل الذي يشير إلى عدد الصفحات
// وستُستبدل بقيمة ثابتة تساوي عدد الصفحات.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// السلوك المعدَّل:
// يتم إعادة تعيين ترقيم الصفحات المستخرج ويبدأ ترقيم جديد،
// كما لو أننا نسخنا محتويات الصفحة الثانية ولصقناها في مستند جديد.
// سيتم تعيين صفحة البداية إلى 1 وسيُترك الحقل الذي يشير إلى عدد الصفحات دون تغيير
// وسيظهر عدد الصفحات الحالي.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
