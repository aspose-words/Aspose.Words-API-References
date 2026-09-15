---
title: "طريقة Aspose::Words::Document::AppendDocument"
linktitle: "AppendDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::AppendDocument. تُضيف المستند المحدد إلى نهاية هذا المستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/document/appenddocument/
---
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


يضيف المستند المحدد إلى نهاية هذا المستند.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | المستند المراد إلحاقه. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |

## أمثلة



يوضح كيفية إلحاق مستند بنهاية مستند آخر.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
srcDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Source document text. ");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
dstDoc->get_FirstSection()->get_Body()->AppendParagraph(u"Destination document text. ");

// ألحق المستند المصدر بالمستند الهدف مع الحفاظ على تنسيقه،
// ثم احفظ المستند المصدر على نظام الملفات المحلي.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting);

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendDocument.docx");
```


يوضح كيفية إلحاق جميع المستندات في مجلد بنهاية مستند قالب.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Template Document");
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Some content here");

// ألحق جميع المستندات غير المشفرة ذات الامتداد .doc
// من دليل نظام الملفات المحلي إلى المستند الأساسي.
System::SharedPtr<System::Collections::Generic::List<System::String>> docFiles = System::IO::Directory::GetFiles(get_MyDir(), u"*.doc")->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String item)>>([](System::String item) -> bool
{
    return item.EndsWith(u".doc");
})))->LINQ_ToList();
for (auto&& fileName : docFiles)
{
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(fileName);
    if (info->get_IsEncrypted())
    {
        continue;
    }

    auto srcDoc = System::MakeObject<Aspose::Words::Document>(fileName);
    dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles);
}

dstDoc->Save(get_ArtifactsDir() + u"Document.AppendAllDocumentsInFolder.doc");
```

## انظر أيضًا

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::AppendDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


يضيف المستند المحدد إلى نهاية هذا المستند.

```cpp
void Aspose::Words::Document::AppendDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | المستند المراد إلحاقه. |
| importFormatMode | Aspose::Words::ImportFormatMode | يحدد كيفية دمج تنسيق الأنماط المتصادمة. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | يسمح بتحديد الخيارات التي تؤثر على تنسيق المستند الناتج. |

## أمثلة



يوضح كيفية إدارة تصادم أنماط القوائم أثناء إلحاق مستند.
```cpp
// حمّل مستندًا بنص في نمط مخصص ونسخه.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom list numbering.docx");
System::SharedPtr<Aspose::Words::Document> dstDoc = srcDoc->Clone();

// لدينا الآن مستندان، كل منهما يحتوي على نمط متماثل يُدعى "CustomStyle".
// غيّر لون النص لأحد الأنماط لتمييزه عن الآخر.
dstDoc->get_Styles()->idx_get(u"CustomStyle")->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

// إذا كان هناك تصادم في أنماط القوائم، فطبق تنسيق القائمة من المستند المصدر.
// عيّن الخاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قوائم إلى المستند الهدف.
// عيّن الخاصية "KeepSourceNumbering" إلى "true" لاستيراد جميع المتصادمة
// ترقيم أنماط القوائم بنفس المظهر الذي كان عليه في المستند المصدر.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);

// دمج مستندين يحتويان على أنماط مختلفة تشترك في نفس الاسم يسبب تصادمًا في الأنماط.
// يمكننا تحديد وضع تنسيق الاستيراد أثناء إلحاق المستندات لحل هذا التصادم.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepDifferentStyles, options);
dstDoc->UpdateListLabels();

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```


يوضح كيفية إدارة تصادم أنماط القوائم أثناء إدراج مستند.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

dstDoc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
System::SharedPtr<Aspose::Words::Lists::List> list = dstDoc->get_Lists()->idx_get(0);

builder->get_ListFormat()->set_List(list);

for (int32_t i = 1; i <= 15; i++)
{
    builder->Write(System::String::Format(u"List Item {0}\n", i));
}

auto attachDoc = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(dstDoc)->Clone(true));

// إذا كان هناك تصادم في أنماط القوائم، فطبق تنسيق القائمة من المستند المصدر.
// عيّن الخاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قوائم إلى المستند الهدف.
// عيّن الخاصية "KeepSourceNumbering" إلى "true" لاستيراد جميع المتصادمة
// ترقيم أنماط القوائم بنفس المظهر الذي كان عليه في المستند المصدر.
auto importOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importOptions->set_KeepSourceNumbering(keepSourceNumbering);

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertDocument(attachDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```


يوضح كيفية إدارة تصادم أنماط القوائم أثناء إلحاق نسخة من مستند بنفسه.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// إذا كان هناك تصادم في أنماط القوائم، فطبق تنسيق القائمة من المستند المصدر.
// عيّن الخاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قوائم إلى المستند الهدف.
// عيّن الخاصية "KeepSourceNumbering" إلى "true" لاستيراد جميع المتصادمة
// ترقيم أنماط القوائم بنفس المظهر الذي كان عليه في المستند المصدر.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_KeepSourceNumbering(keepSourceNumbering);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->UpdateListLabels();
```

## انظر أيضًا

* Class [Document](../)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
