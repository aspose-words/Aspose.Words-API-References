---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional metodo"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional metodo. Specifica se scrivere la dichiarazione DOCTYPE durante il salvataggio in HTML o MHTML. Quando true, scrive una dichiarazione DOCTYPE nel documento prima dell'elemento radice. Il valore predefinito è false. Quando si salva in EPUB o HTML5 (Html5) la dichiarazione DOCTYPE viene sempre scritta in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


Specifica se scrivere la dichiarazione DOCTYPE durante il salvataggio in HTML o MHTML. Quando **true**, scrive una dichiarazione DOCTYPE nel documento prima dell'elemento radice. Il valore predefinito è **false**. Quando si salva in EPUB o HTML5 ([Html5](../../htmlversion/)) la dichiarazione DOCTYPE viene sempre scritta.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Note


Aspose.Words scrive sempre HTML ben formato indipendentemente da questa impostazione.

Quando **true**, l'inizio del documento HTML di output avrà questo aspetto:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words mira a produrre XHTML secondo la specifica XHTML 1.0 Transitional, ma l'output non sempre convalida contro il DTD. Alcune strutture all'interno di un documento Microsoft Word sono difficili o impossibili da mappare a un documento che convalidi contro lo schema XHTML. Per esempio, XHTML non consente liste annidate (UL non può essere annidata all'interno di un altro elemento UL), ma nei documenti Microsoft Word le liste multilevel si verificano abbastanza spesso.

## Esempi



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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
