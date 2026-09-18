---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText-Methode"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText-Methode. Steuert, wie Texteingabe‑Formularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist false in C++."
type: docs
weight: 28000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


Steuert, wie Texteingabe-Formularfelder nach HTML oder MHTML gespeichert werden. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## Hinweise


Wenn auf **true** gesetzt, werden Texteingabe‑Formularfelder als normaler Text exportiert. Wenn auf **false** gesetzt, werden Word‑Texteingabe‑Formularfelder als INPUT‑Elemente in HTML exportiert.

Beim Export nach EPUB werden Texteingabe‑Formularfelder aufgrund der Anforderungen dieses Formats immer als Text gespeichert.

## Beispiele



Zeigt, wie man den Ordner zum Speichern verknüpfter Bilder nach dem Speichern als .html angibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Setzt eine Option, um Formularfelder als Klartext anstelle von HTML-Eingabeelementen zu exportieren.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
