---
title: "Aspose::Words::Saving::DocumentSplitCriteria Aufzählung"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocumentSplitCriteria Aufzählung. Gibt an, wie das Dokument beim Speichern im Html-, Epub‑ oder Azw3‑Format in C++ in Teile aufgeteilt wird."
type: docs
weight: 52000
url: /de/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Gibt an, wie das Dokument beim Speichern in das [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) oder [Azw3](../../aspose.words/saveformat/) Format in Teile aufgeteilt wird.

```cpp
enum class DocumentSplitCriteria
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Das Dokument wird nicht aufgeteilt. |
| PageBreak | 1 | Das Dokument wird an expliziten Seitenumbrüchen in Teile aufgeteilt. Ein Seitenumbruch kann durch ein [PageBreak](../../aspose.words/controlchar/pagebreak/) Zeichen, einen Abschnittswechsel, der den Beginn eines neuen Abschnitts auf einer neuen Seite angibt, oder einen Absatz, dessen [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) Eigenschaft auf **true** gesetzt ist, spezifiziert werden. |
| ColumnBreak | 2 | Das Dokument wird an Spaltenumbrüchen in Teile aufgeteilt. Ein Spaltenumbruch kann durch ein [ColumnBreak](../../aspose.words/controlchar/columnbreak/) Zeichen oder einen Abschnittswechsel, der den Beginn eines neuen Abschnitts in einer neuen Spalte angibt, spezifiziert werden. |
| SectionBreak | 4 | Das Dokument wird an einem Abschnittswechsel beliebigen Typs in Teile aufgeteilt. |
| HeadingParagraph | 8 | Das Dokument wird an einem Absatz, der mit einer Überschriftenformatierung **Heading 1**, **Heading 2** usw. formatiert ist, in Teile aufgeteilt. Verwenden Sie zusammen mit [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/), um die Überschriftenebenen (von 1 bis zur angegebenen Ebene) anzugeben, bei denen aufgeteilt werden soll. |

## Hinweise


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Verschiedene Kriterien können teilweise überlappen. Zum Beispiel wird dem **Heading 1**‑Stil häufig die [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/)‑Eigenschaft zugewiesen, sodass er unter zwei Kriterien fällt: [PageBreak](./) und [HeadingParagraph](./). Einige Abschnittswechsel können Seitenumbrüche verursachen und so weiter. In typischen Fällen ist das Angeben nur einer Flagge die praktischste Option.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
