---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles طريقة"
linktitle: "get_ForceCopyStyles"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles طريقة. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان سيتم نسخ الأنماط المتضاربة في وضع KeepSourceFormatting. القيمة الافتراضية هي false في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان سيتم نسخ الأنماط المتضاربة في وضع [KeepSourceFormatting](../../importformatmode/). القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## ملاحظات


بشكل افتراضي، إذا كان هناك نمط مطابق موجود بالفعل في مستند الوجهة، يتم توسيع تنسيق نمط المصدر إلى سمات العقدة المباشرة ويتم إعادة تعيين نمط هذه العقدة إلى القيمة الافتراضية.

عند تعيين هذا الخيار إلى **true**، سيتم نسخ نمط المصدر قسرًا إلى مستند الوجهة باسم فريد وتطبيقه على العقدة المستوردة.

ملاحظة، في هذه الحالة لا يُضمن الحفاظ على تنسيق العقدة المستوردة في مستند الوجهة.

## أمثلة



يوضح كيفية نسخ أنماط المصدر بأسماء فريدة قسرًا.
```cpp
// كلا المستندين يحتويان على MyStyle1 و MyStyle2، بينما MyStyle3 موجود فقط في مستند المصدر.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
