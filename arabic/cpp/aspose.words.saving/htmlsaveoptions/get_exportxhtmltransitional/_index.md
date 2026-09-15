---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional"
linktitle: "get_ExportXhtmlTransitional"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional. يحدد ما إذا كان يجب كتابة إعلان DOCTYPE عند الحفظ إلى HTML أو MHTML. عندما **true**، يكتب إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هي **false**. عند الحفظ إلى EPUB أو HTML5 (Html5) يتم دائمًا كتابة إعلان DOCTYPE في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


يحدد ما إذا كان يجب كتابة إعلان DOCTYPE عند الحفظ إلى HTML أو MHTML. عندما **true**، يكتب إعلان DOCTYPE في المستند قبل العنصر الجذر. القيمة الافتراضية هي **false**. عند الحفظ إلى EPUB أو HTML5 ([Html5](../../htmlversion/)) يتم دائمًا كتابة إعلان DOCTYPE.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## ملاحظات


Aspose.Words دائمًا يكتب HTML مُشكل بشكل صحيح بغض النظر عن هذا الإعداد.

عندما **true**، سيبدو بداية مستند HTML الناتج هكذا:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


تهدف Aspose.Words إلى إنتاج XHTML وفقًا لمواصفات XHTML 1.0 Transitional، لكن الناتج لا يتحقق دائمًا من صحة DTD. بعض البُنى داخل مستند Microsoft Word يصعب أو يستحيل تحويلها إلى مستند يطابق مخطط XHTML. على سبيل المثال، لا يسمح XHTML بالقوائم المتداخلة (لا يمكن أن تكون UL داخل عنصر UL آخر)، لكن القوائم متعددة المستويات تظهر كثيرًا في مستندات Microsoft Word.

## أمثلة



يوضح كيفية عرض عنوان DOCTYPE عند تحويل المستندات إلى معيار Xhtml 1.0 الانتقالي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// سيتضمن مستندنا عنوان إعلان DOCTYPE فقط إذا قمنا بتعيين العلامة "ExportXhtmlTransitional" إلى "true".
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
