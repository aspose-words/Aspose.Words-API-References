---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion metodo"
linktitle: "get_HtmlVersion"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion metodo. Specifica la versione dello standard HTML da utilizzare quando si salva il documento in HTML o MHTML. Il valore predefinito è Xhtml in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_htmlversion/
---
## HtmlSaveOptions::get_HtmlVersion method


Specifica la versione dello standard HTML da utilizzare quando si salva il documento in HTML o MHTML. Il valore predefinito è [Xhtml](../../htmlversion/).

```cpp
Aspose::Words::Saving::HtmlVersion Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion() const
```


## Esempi



Mostra come salvare un documento in una versione specifica di HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html", options);

// I nostri documenti HTML avranno piccole differenze per essere compatibili con diverse versioni di HTML.
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case Aspose::Words::Saving::HtmlVersion::Html5:
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;

    case Aspose::Words::Saving::HtmlVersion::Xhtml:
        ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;

}
```


Mostra come visualizzare un'intestazione DOCTYPE durante la conversione dei documenti allo standard Xhtml 1.0 transitional.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Il nostro documento conterrà solo un'intestazione di dichiarazione DOCTYPE se abbiamo impostato il flag "ExportXhtmlTransitional" su "true".
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

## Vedi anche

* Enum [HtmlVersion](../../htmlversion/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
