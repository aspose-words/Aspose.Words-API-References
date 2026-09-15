---
title: "طريقة Aspose::Words::Document::ExtractPages"
linktitle: "ExtractPages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::ExtractPages. تُرجع كائن Document الذي يمثل النطاق المحدد من الصفحات في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


تُرجع كائن [Document](../) الذي يمثل النطاق المحدد من الصفحات.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| count | int32_t | عدد الصفحات التي سيتم استخراجها. |

## أمثلة



يوضح كيفية الحصول على النطاق المحدد من الصفحات من المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


يعيد كائن [Document](../) الذي يمثل النطاق المحدد من الصفحات وخيارات استخراج الصفحات المعطاة.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للصفحة الأولى التي سيتم استخراجها. |
| count | int32_t | عدد الصفحات التي سيتم استخراجها. |
| خيارات | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | يوفر خيارات لإدارة عملية استخراج الصفحات. |

## انظر أيضًا

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
