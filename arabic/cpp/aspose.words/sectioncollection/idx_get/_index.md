---
title: "Aspose::Words::SectionCollection::idx_get طريقة"
linktitle: "idx_get"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::SectionCollection::idx_get طريقة. تسترجع قسمًا عند الفهرس المحدد في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/sectioncollection/idx_get/
---
## SectionCollection::idx_get method


يسترجع section عند الفهرس المحدد.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::SectionCollection::idx_get(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس في قائمة الأقسام. |
## ملاحظات


الفهرس يبدأ من الصفر.

يسمح باستخدام الفهارس السلبية وتدل على الوصول من نهاية المجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني العنصر قبل الأخير، وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فإن هذا يُرجع إشارة فارغة.

إذا كان الفهرس سالبًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فإن هذا يُرجع إشارة فارغة.

## أمثلة



يظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// حفظ المستند إلى PDF أو إلى صورة أو طباعته للمرة الأولى سيؤدي تلقائيًا
// لتخزين تخطيط المستند داخل صفحاته في الذاكرة المؤقتة.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// تعديل المستند بطريقة ما.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// في الإصدار الحالي من Aspose.Words، تعديل المستند لا يعيد بناءه تلقائيًا
// تخطيط الصفحة المخزّن مؤقتًا. إذا أردنا أن يكون التخطيط المخزّن مؤقتًا
// للبقاء محدثًا، سنحتاج إلى تحديثه يدويًا.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```


يوضح كيفية إعداد عقدة قسم جديدة للتحرير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يأتي مستند فارغ مع قسم، يحتوي على جسم، والذي بدوره يحتوي على فقرة.
// يمكننا إضافة محتويات إلى هذا المستند عن طريق إضافة عناصر مثل مقاطع النص، الأشكال، أو الجداول إلى تلك الفقرة.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// إذا أضفنا قسمًا جديدًا بهذه الطريقة، فلن يحتوي على جسم أو أي عقد أطفال أخرى.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// شغّل طريقة "EnsureMinimum" لإضافة جسم وفقرة إلى هذا القسم لبدء تحريره.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Section](../../section/)
* Class [SectionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
