---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation"
linktitle: "get_ExportLanguageInformation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation. Specifica se le informazioni sulla lingua vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è false in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Specifica se le informazioni sulla lingua vengono esportate in HTML, MHTML o EPUB. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Note


Quando questa proprietà è impostata su **true**, Aspose.Words genera l'attributo HTML **lang** sugli elementi del documento che specificano la lingua. Questo può essere necessario per preservare la semantica legata alla lingua.

## Esempi



Mostra come preservare le informazioni sulla lingua durante il salvataggio in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilizza il builder per scrivere testo formattandolo in diverse impostazioni locali.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// Quando si salva il documento in HTML, possiamo passare un oggetto SaveOptions
// per preservare o scartare la localizzazione di ciascun testo formattato.
// Se impostiamo il flag "ExportLanguageInformation" su "true",
// il documento HTML di output conterrà le impostazioni locali negli attributi "lang" dei tag <span>.
// Se impostiamo il flag "ExportLanguageInformation" su "false',
// il testo nel documento HTML di output non conterrà alcuna informazione sulla localizzazione.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
