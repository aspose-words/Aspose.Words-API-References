---
title: "طريقة Aspose::Words::DocumentBase::ImportNode"
linktitle: "ImportNode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBase::ImportNode. تستورد عقدة من مستند آخر إلى المستند الحالي بلغة C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


يستورد عقدة من مستند آخر إلى المستند الحالي.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة التي يتم استيرادها. |
| isImportChildren | bool | **true** لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا، **false**. |

### ReturnValue

العقدة المستنسخة التي تنتمي إلى المستند الحالي.
## ملاحظات


تستخدم هذه الطريقة الخيار [UseDestinationStyles](../../importformatmode/) لحل تنسيق النص.

استيراد عقدة ينشئ نسخة من العقدة المصدر التي تنتمي إلى المستند المستورد. العقدة المرتجعة لا تحتوي على أصل. العقدة المصدر لا تُعدَّل أو تُزال من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند الخاصة مثل الإشارات إلى الأنماط والقوائم من الأصلي إلى المستند المستورد. بعد استيراد العقدة، يمكن إدراجها في الموضع المناسب في المستند باستخدام [InsertBefore1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء نسخة عميقة من العقدة المصدر.

## أمثلة



يوضح كيفية استيراد عقدة من مستند إلى آخر.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// كل عقدة لها مستند أصل، وهو المستند الذي يحتوي على العقدة.
// إدراج عقدة في مستند لا تنتمي إليه العقدة سيؤدي إلى رمي استثناء.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// استخدم طريقة ImportNode لإنشاء نسخة من عقدة، والتي ستحمل المستند
// الذي استدعى طريقة ImportNode يحدد كمستند مالك جديد له.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// يمكننا الآن إدراج العقدة في المستند.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة للاستيراد. |
| isImportChildren | bool | **true** لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا، **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |

### ReturnValue

العقدة المستنسخة والمستوردة. العقدة تنتمي إلى المستند الوجهة، ولكن لا أصل لها.
## ملاحظات


هذا التحميل الزائد مفيد للتحكم في كيفية استيراد الأنماط وتنسيق القوائم.

استيراد عقدة ينشئ نسخة من العقدة المصدر التي تنتمي إلى المستند المستورد. العقدة المرتجعة لا تحتوي على أصل. العقدة المصدر لا تُعدَّل أو تُزال من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند الخاصة مثل الإشارات إلى الأنماط والقوائم من الأصلي إلى المستند المستورد. بعد استيراد العقدة، يمكن إدراجها في الموضع المناسب في المستند باستخدام [InsertBefore1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء نسخة عميقة من العقدة المصدر.

## أمثلة



يوضح كيفية استيراد عقدة من المستند المصدر إلى المستند الوجهة باستخدام خيارات محددة.
```cpp
// أنشئ مستندين وأضف نمط حرف إلى كل مستند.
// قم بتكوين الأنماط لتكون لها نفس الاسم، ولكن بتنسيق نص مختلف.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// استورد القسم من المستند الوجهة إلى المستند المصدر، مما يسبب تصادمًا في اسم النمط.
// إذا استخدمنا أنماط الوجهة، فإن النص المصدر المستورد الذي يحمل نفس اسم النمط
// كالنص الوجهة سيتبنى نمط الوجهة.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// إذا استخدمنا ImportFormatMode.KeepDifferentStyles، سيُحفظ النمط المصدر،
// وسيتم حل تصادم الأسماء بإضافة لاحقة.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## انظر أيضًا

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


يستورد عقدة من مستند آخر إلى المستند الحالي مع خيار للتحكم في التنسيق.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة للاستيراد. |
| isImportChildren | bool | **true** لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا، **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | يسمح بتحديد خيارات تنسيق إضافية متنوعة. |

### ReturnValue

العقدة المستنسخة والمستوردة. العقدة تنتمي إلى المستند الوجهة، ولكن لا أصل لها.
## ملاحظات


هذا التحميل الزائد مفيد للتحكم في كيفية استيراد الأنماط وتنسيق القوائم.

استيراد عقدة ينشئ نسخة من العقدة المصدر التي تنتمي إلى المستند المستورد. العقدة المرتجعة لا تحتوي على أصل. العقدة المصدر لا تُعدَّل أو تُزال من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند الخاصة مثل الإشارات إلى الأنماط والقوائم من الأصلي إلى المستند المستورد. بعد استيراد العقدة، يمكن إدراجها في الموضع المناسب في المستند باستخدام [InsertBefore1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء نسخة عميقة من العقدة المصدر.

## أمثلة



يوضح كيفية استيراد عقدة مع حل ألوان سمة المصدر للأشكال.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// انتقل إلى التذييل الأساسي وأدرج شكلاً يستخدم ألوان السمة.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// استورد تذييل المصدر إلى المستند الوجهة مع حل ألوان السمة،
// بحيث يحتفظ الشكل لونه الفعلي من المستند المصدر.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## انظر أيضًا

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
