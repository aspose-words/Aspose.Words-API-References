---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText metodo"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText metodo. Controlla come i campi di input di testo del modulo vengono salvati in HTML o MHTML. Il valore predefinito è false in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Controlla come i campi di modulo di input di testo vengono salvati in HTML o MHTML. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Note


Quando impostato su **true**, esporta i campi di input di testo del modulo come testo normale. Quando **false**, esporta i campi di input di testo di Word come elementi INPUT in HTML.

Durante l'esportazione in EPUB, i campi di input di testo del modulo vengono sempre salvati come testo a causa dei requisiti di questo formato.

## Esempi



Mostra come specificare la cartella per memorizzare le immagini collegate dopo il salvataggio in .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Imposta un'opzione per esportare i campi modulo come testo semplice invece di elementi di input HTML.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
