---
title: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering method"
linktitle: "get_KeepSourceNumbering"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering method. يحصل على أو يضبط قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في المستندات المصدر والهدف. القيمة الافتراضية هي false في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/importformatoptions/get_keepsourcenumbering/
---
## ImportFormatOptions::get_KeepSourceNumbering method


يحصل أو يضبط قيمة منطقية تحدد كيفية استيراد الترقيم عندما يتصادم في مستندات المصدر والوجهة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering() const
```


## أمثلة



يعرض كيفية استيراد مستند يحتوي على قوائم مرقمة.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

ASSERT_EQ(4, dstDoc->get_Lists()->get_Count());

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();

// إذا كان هناك تصادم في أنماط القوائم، فطبق تنسيق القائمة من المستند المصدر.
// عيّن الخاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قوائم إلى المستند الهدف.
// عيّن الخاصية "KeepSourceNumbering" إلى "true" لاستيراد جميع المتصادمة
// ترقيم أنماط القوائم بنفس المظهر الذي كان عليه في المستند المصدر.
options->set_KeepSourceNumbering(isKeepSourceNumbering);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);
dstDoc->UpdateListLabels();

ASSERT_EQ(isKeepSourceNumbering ? 5 : 4, dstDoc->get_Lists()->get_Count());
```


يعرض كيفية حل التعارض عند استيراد مستندات تحتوي على قوائم بنفس معرف تعريف القائمة.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with the same definition identifier - destination.docx");

// قم بتعيين الخاصية "KeepSourceNumbering" إلى "true" لتطبيق معرف تعريف قائمة مختلف.
// لأنماط متطابقة كما تستوردها Aspose.Words إلى المستندات الهدف.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


يعرض كيفية حل تعارضات ترقيم القوائم في المستندات المصدر والهدف.
```cpp
// افتح مستندًا يحتوي على مخطط ترقيم قوائم مخصص، ثم استنسخه.
// نظرًا لأن كلاهما يمتلك نفس تنسيق الترقيم، سيتصادم التنسيقان إذا استوردنا مستندًا واحدًا إلى الآخر.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// عند استيراد نسخة المستند إلى الأصل ثم إلحاقها،
// سيتحد القائمتان ذات نفس تنسيق القائمة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" إلى "false"، فإن القائمة من نسخة المستند
// التي نلحقها بالأصل ستستمر في ترقيم القائمة التي نلحقها إليها.
// سيؤدي ذلك إلى دمج القائمتين في قائمة واحدة فعليًا.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" إلى "true"، فإن نسخة المستند
// ستحافظ القائمة على ترقيمها الأصلي، مما يجعل القائمتين تظهران كقوائم منفصلة.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = System::MakeObject<Aspose::Words::NodeImporter>(srcDoc, dstDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    System::SharedPtr<Aspose::Words::Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Node>>(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(System::String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" + u"12. Item 3\r\n" + u"13. Item 4", dstDoc->get_FirstSection()->get_Body()->ToString(Aspose::Words::SaveFormat::Text).Trim());
}
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
