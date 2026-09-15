---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText method"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText. تتحكم في كيفية حفظ حقول نماذج إدخال النص إلى HTML أو MHTML. القيمة الافتراضية هي false في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


يتحكم في كيفية حفظ حقول نماذج إدخال النص إلى HTML أو MHTML. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## ملاحظات


عند تعيينه إلى **true**، يتم تصدير حقول نماذج إدخال النص كنص عادي. وعند تعيينه إلى **false**، يتم تصدير حقول نماذج إدخال النص في Word كعناصر INPUT في HTML.

عند التصدير إلى EPUB، يتم دائمًا حفظ حقول نماذج إدخال النص كنص بسبب متطلبات هذا التنسيق.

## أمثلة



يوضح كيفية تحديد المجلد لتخزين الصور المرتبطة بعد الحفظ إلى .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// حدد خيارًا لتصدير حقول النموذج كنص عادي بدلاً من عناصر إدخال HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
