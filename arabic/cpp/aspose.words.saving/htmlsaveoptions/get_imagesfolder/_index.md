---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder طريقة"
linktitle: "get_ImagesFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder طريقة. يحدد المجلد الفعلي حيث تُحفظ الصور عند تصدير مستند إلى صيغة HTML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


يحدد المجلد الفعلي حيث تُحفظ الصور عند تصدير مستند إلى صيغة HTML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## ملاحظات


عند حفظك لـ [Document](../../../aspose.words/document/) بصيغة HTML، يحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. يتيح لك [ImagesFolder](./) تحديد مكان حفظ الصور و[ImagesFolderAlias](../get_imagesfolderalias/) تحديد كيفية بناء عناوين URI للصور.

إذا حفظت مستندًا في ملف وقدمت اسم ملف، يقوم Aspose.Words، بشكل افتراضي، بحفظ الصور في نفس المجلد الذي يُحفظ فيه ملف المستند. استخدم [ImagesFolder](./) لتجاوز هذا السلوك.

إذا حفظت مستندًا في تدفق، لا يمتلك Aspose.Words مجلدًا لحفظ الصور، لكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في خاصية [ImagesFolder](./) أو توفير تدفقات مخصصة عبر معالج الحدث [ImageSavingCallback](../get_imagesavingcallback/).

إذا كان المجلد المحدد بواسطة [ImagesFolder](./) غير موجود، سيتم إنشاؤه تلقائيًا.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

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
