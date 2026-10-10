---
title: "Aspose::Words::NodeImporter::NodeImporter منشئ"
linktitle: "NodeImporter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeImporter::NodeImporter منشئ. يقوم بتهيئة نسخة جديدة من فئة NodeImporter في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) constructor


يقوم بتهيئة نسخة جديدة من الفئة [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المصدر. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند الهدف الذي سيكون مالك العقد المستوردة. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |

## انظر أيضًا

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## NodeImporter::NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) constructor


يقوم بتهيئة نسخة جديدة من الفئة [NodeImporter](../).

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المصدر. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند الهدف الذي سيكون مالك العقد المستوردة. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | يحدد خيارات متعددة لتنسيق العقد المستوردة. |

## أمثلة



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

* Class [DocumentBase](../../documentbase/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
