---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText метод"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText метод. Управляет тем, как сохраняются текстовые поля ввода в HTML или MHTML. Значение по умолчанию — false в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Управляет тем, как текстовые поля формы сохраняются в HTML или MHTML. Значение по умолчанию **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Примечания


Когда установлено в **true**, экспортирует текстовые поля ввода как обычный текст. Когда **false**, экспортирует текстовые поля ввода Word как элементы INPUT в HTML.

При экспорте в EPUB текстовые поля ввода всегда сохраняются как текст из‑за требований этого формата.

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
