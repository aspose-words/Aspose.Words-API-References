---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding Methode"
linktitle: "get_Encoding"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_Encoding Methode. Gibt die zu verwendende Kodierung beim Exportieren nach HTML, MHTML oder EPUB an. Der Standardwert ist new UTF8Encoding(false) (UTF‑8 ohne BOM) in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_encoding/
---
## HtmlSaveOptions::get_Encoding method


Gibt die zu verwendende Kodierung beim Export nach HTML, MHTML oder EPUB an. Der Standardwert ist **new UTF8Encoding(false)** (UTF-8 ohne BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlSaveOptions::get_Encoding() const
```


## Beispiele



Zeigt, wie beim Speichern eines Dokuments als .epub eine bestimmte Kodierung verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Verwenden Sie ein SaveOptions‑Objekt, um die Kodierung für ein Dokument, das wir speichern werden, anzugeben.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Standardmäßig enthält ein ausgegebenes .epub‑Dokument alle Inhalte in einem HTML‑Teil.
// Ein Aufteilungskriterium ermöglicht es uns, das Dokument in mehrere HTML‑Teile zu segmentieren.
// Wir werden die Kriterien festlegen, um das Dokument in Überschrifts‑Absätze aufzuteilen.
// Dies ist nützlich für Leser, die HTML‑Dateien, die größer als eine bestimmte Größe sind, nicht lesen können.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
