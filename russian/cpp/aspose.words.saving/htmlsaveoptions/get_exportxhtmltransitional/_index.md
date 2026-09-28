---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional метод"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional метод. Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. Когда **true**, записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию — **false**. При сохранении в EPUB или HTML5 (Html5) объявление DOCTYPE всегда записывается в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. Когда **true**, записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию — **false**. При сохранении в EPUB или HTML5 ([Html5](../../htmlversion/)) объявление DOCTYPE всегда записывается.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Примечания


Aspose.Words всегда генерирует корректный HTML независимо от этой настройки.

Когда **true**, начало выходного HTML‑документа будет выглядеть так:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words стремится выводить XHTML в соответствии со спецификацией XHTML 1.0 Transitional, но полученный документ не всегда проходит проверку по DTD. Некоторые структуры внутри документа Microsoft Word трудно или невозможно отобразить в документе, который будет валидным по схеме XHTML. Например, XHTML не допускает вложенные списки (UL не может быть вложен в другой элемент UL), однако в документах Microsoft Word многоуровневые списки встречаются довольно часто.

## Примеры



Показывает, как отобразить заголовок DOCTYPE при конвертации документов в стандарт Xhtml 1.0 transitional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Наш документ будет содержать заголовок декларации DOCTYPE только если мы установили флаг "ExportXhtmlTransitional" в значение "true".
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

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
