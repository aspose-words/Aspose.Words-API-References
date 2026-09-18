---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties Methode"
linktitle: "get_ExportDocumentProperties"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties Methode. Gibt an, ob integrierte und benutzerdefinierte Dokumenteigenschaften nach HTML, MHTML oder EPUB exportiert werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportdocumentproperties/
---
## HtmlSaveOptions::get_ExportDocumentProperties method


Gibt an, ob integrierte und benutzerdefinierte Dokumenteigenschaften nach HTML, MHTML oder EPUB exportiert werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties() const
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
