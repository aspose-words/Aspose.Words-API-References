---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder метод"
linktitle: "get_ImagesFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder метод. Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию это пустая строка в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Указывает физическую папку, в которой изображения сохраняются при экспорте документа в формат HTML. По умолчанию пустая строка.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в формате HTML, Aspose.Words необходимо сохранять все изображения, встроенные в документ, как отдельные файлы. [ImagesFolder](./) позволяет указать, где будут сохраняться изображения, а [ImagesFolderAlias](../get_imagesfolderalias/) позволяет задать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранён файл документа. Используйте [ImagesFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения изображений, но всё равно необходимо где‑то их сохранять. В этом случае следует указать доступную папку в свойстве [ImagesFolder](./) или предоставить пользовательские потоки через обработчик события [ImageSavingCallback](../get_imagesavingcallback/).

Если папка, указанная в [ImagesFolder](./), не существует, она будет создана автоматически.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## Примеры



Показывает, как указать папку для хранения связанных изображений после сохранения в .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Установите параметр для экспорта полей формы как обычный текст вместо HTML‑элементов ввода.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
