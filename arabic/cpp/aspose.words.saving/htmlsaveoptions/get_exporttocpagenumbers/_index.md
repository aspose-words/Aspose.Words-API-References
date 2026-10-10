---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers"
linktitle: "get_ExportTocPageNumbers"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers. تحدد ما إذا كان يجب كتابة أرقام الصفحات إلى جدول المحتويات عند حفظ HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


يحدد ما إذا كان يجب كتابة أرقام الصفحات إلى جدول المحتويات عند حفظ HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## أمثلة



يوضح كيفية عرض أرقام الصفحات عند حفظ مستند يحتوي على جدول محتويات إلى .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج جدول محتويات، ثم عبّئ المستند بفقرات مُنسقة باستخدام "Heading"
// النمط الذي سيختاره جدول المحتويات كعناصر. كل عنصر سيعرض فقرة العنوان على اليسار،
// ورقم الصفحة الذي يحتوي على العنوان على اليمين.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// مستندات HTML لا تحتوي على صفحات. إذا حفظنا هذا المستند إلى HTML،
// ستكون أرقام الصفحات التي يعرضها جدول المحتويات لدينا بلا معنى.
// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions لتجاهل أرقام الصفحات هذه من جدول المحتويات.
// إذا قمنا بتعيين علامة "ExportTocPageNumbers" إلى "true",
// كل عنصر في جدول المحتويات سيعرض العنوان والفاصل ورقم الصفحة، مع الحفاظ على مظهره في Microsoft Word.
// إذا قمنا بتعيين علامة "ExportTocPageNumbers" إلى "false",
// ستتجاهل عملية الحفظ كلًا من الفاصل ورقم الصفحة وتترك العنوان لكل عنصر كما هو.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
