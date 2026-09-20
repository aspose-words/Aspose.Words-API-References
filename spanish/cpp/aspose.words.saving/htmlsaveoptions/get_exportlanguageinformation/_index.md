---
title: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation"
linktitle: "get_ExportLanguageInformation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation. Especifica si la información de idioma se exporta a HTML, MHTML o EPUB. El valor predeterminado es false en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


Especifica si la información de idioma se exporta a HTML, MHTML o EPUB. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## Observaciones


Cuando esta propiedad se establece en **true**, Aspose.Words genera el atributo HTML **lang** en los elementos del documento que especifican el idioma. Esto puede ser necesario para preservar la semántica relacionada con el idioma.

## Ejemplos



Muestra cómo preservar la información de idioma al guardar en .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilice el generador para escribir texto mientras lo formatea en diferentes configuraciones regionales.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// Al guardar el documento en HTML, podemos pasar un objeto SaveOptions
// para preservar o descartar la configuración regional de cada texto formateado.
// Si establecemos la bandera "ExportLanguageInformation" a "true",
// el documento HTML de salida contendrá las configuraciones regionales en los atributos "lang" de las etiquetas <span>.
// Si establecemos la bandera "ExportLanguageInformation" a "false',
// el texto en el documento HTML de salida no contendrá ninguna información de configuración regional.
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

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
