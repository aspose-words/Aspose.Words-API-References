---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional Methode"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional Methode. Gibt an, ob beim Speichern in HTML oder MHTML die DOCTYPE‑Deklaration geschrieben werden soll. Wenn true, wird eine DOCTYPE‑Deklaration im Dokument vor dem Wurzelelement geschrieben. Der Standardwert ist false. Beim Speichern in EPUB oder HTML5 (Html5) wird die DOCTYPE‑Deklaration immer in C++ geschrieben."
type: docs
weight: 30000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


Gibt an, ob beim Speichern in HTML oder MHTML die DOCTYPE‑Deklaration geschrieben werden soll. Wenn **true**, wird eine DOCTYPE‑Deklaration im Dokument vor dem Wurzelelement geschrieben. Der Standardwert ist **false**. Beim Speichern in EPUB oder HTML5 ([Html5](../../htmlversion/)) wird die DOCTYPE‑Deklaration immer geschrieben.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## Hinweise


Aspose.Words erzeugt stets wohlgeformtes HTML, unabhängig von dieser Einstellung.

Wenn **true**, sieht der Beginn des HTML‑Ausgabedokuments folgendermaßen aus:


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words zielt darauf ab, XHTML gemäß der XHTML 1.0 Transitional‑Spezifikation auszugeben, aber die Ausgabe wird nicht immer gegen die DTD validieren. Einige Strukturen in einem Microsoft‑Word‑Dokument lassen sich nur schwer oder gar nicht auf ein Dokument abbilden, das gegen das XHTML‑Schema validiert. Beispielsweise erlaubt XHTML keine verschachtelten Listen (UL kann nicht innerhalb eines anderen UL‑Elements verschachtelt werden), doch in Microsoft‑Word‑Dokumenten kommen mehrstufige Listen recht häufig vor.

## Beispiele



Zeigt, wie eine DOCTYPE‑Überschrift angezeigt wird, wenn Dokumente in den Xhtml 1.0 Transitional‑Standard konvertiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Unser Dokument enthält nur eine DOCTYPE-Deklarationsüberschrift, wenn wir das Flag "ExportXhtmlTransitional" auf "true" gesetzt haben.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
