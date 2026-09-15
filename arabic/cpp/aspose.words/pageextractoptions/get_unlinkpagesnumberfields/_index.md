---
title: "get_UnlinkPagesNumberFields"
linktitle: "طريقة Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields. تحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. القيمة الافتراضية هي true في C++."
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageExtractOptions::set_UnlinkPagesNumberFields"
type: docs
weight: 3000
url: /ar/cpp/aspose.words/pageextractoptions/get_unlinkpagesnumberfields/
---
## PageExtractOptions::get_UnlinkPagesNumberFields method


يحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields() const
```


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

* Class [PageExtractOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
