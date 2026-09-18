---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria Methode"
linktitle: "get_DocumentSplitCriteria"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria Methode. Gibt an, wie das Dokument beim Speichern im Html-, Epub- oder Azw3-Format aufgeteilt werden soll. Standard ist None für HTML und HeadingParagraph für EPUB und AZW3 in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Gibt an, wie das Dokument beim Speichern im [Html](../../../aspose.words/saveformat/)-, [Epub](../../../aspose.words/saveformat/)- oder [Azw3](../../../aspose.words/saveformat/)-Format aufgeteilt werden soll. Standard ist [None](../../documentsplitcriteria/) für HTML und [HeadingParagraph](../../documentsplitcriteria/) für EPUB und AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Hinweise


Normalerweise möchte man ein Dokument, das als HTML gespeichert wird, als einzelne Datei haben. In manchen Fällen ist es jedoch vorzuziehen, die Ausgabe in mehrere kleinere HTML‑Seiten aufzuteilen. Beim Speichern im HTML‑Format werden diese Seiten in einzelne Dateien oder Streams ausgegeben. Beim Speichern im EPUB‑Format werden sie in die entsprechenden Pakete eingebettet.

Ein Dokument kann beim Speichern im MHTML-Format nicht aufgeteilt werden.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
