---
title: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum"
linktitle: "TxtExportHeadersFootersMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::TxtExportHeadersFootersMode enum. Gibt an, wie Kopf- und Fußzeilen in das Klartextformat in C++ exportiert werden."
type: docs
weight: 86000
url: /de/cpp/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enum


Gibt an, wie Kopf‑ und Fußzeilen in das Nur‑Text‑Format exportiert werden.

```cpp
enum class TxtExportHeadersFootersMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Keine Kopf- und Fußzeilen werden exportiert. |
| PrimaryOnly | 1 | Nur primäre Kopf- und Fußzeilen werden zu Beginn und am Ende jedes Abschnitts exportiert. |
| AllAtEnd | 2 | Alle Kopf- und Fußzeilen werden nach allen Abschnittsinhalten am ganz Ende eines Dokuments platziert. |


## Beispiele



Zeigt, wie man angibt, wie Kopf- und Fußzeilen in das Klartextformat exportiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Füge gerade und primäre Kopf-/Fußzeilen in das Dokument ein.
// Die primären Kopf-/Fußzeilen überschreiben die geraden Kopf-/Fußzeilen.
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->AppendParagraph(u"Even header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterEven));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->AppendParagraph(u"Even footer");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->AppendParagraph(u"Primary header");
doc->get_FirstSection()->get_HeadersFooters()->Add(System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary));
doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->AppendParagraph(u"Primary footer");

// Füge Seiten ein, um diese Kopf- und Fußzeilen anzuzeigen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Erstelle ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument in Klartext speichern.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Setze die "ExportHeadersFootersMode"-Eigenschaft auf "TxtExportHeadersFootersMode.None"
// um keine Kopf- oder Fußzeilen zu exportieren.
// Setze die "ExportHeadersFootersMode"-Eigenschaft auf "TxtExportHeadersFootersMode.PrimaryOnly"
// um nur primäre Kopf- und Fußzeilen zu exportieren.
// Setze die "ExportHeadersFootersMode"-Eigenschaft auf "TxtExportHeadersFootersMode.AllAtEnd"
// um alle Kopf- und Fußzeilen für alle Abschnittsinhalte am Ende des Dokuments zu platzieren.
saveOptions->set_ExportHeadersFootersMode(txtExportHeadersFootersMode);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.ExportHeadersFooters.txt");

System::String newLine = System::Environment::get_NewLine();
switch (txtExportHeadersFootersMode)
{
    case Aspose::Words::Saving::TxtExportHeadersFootersMode::AllAtEnd:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Even header{0}{1}", newLine, newLine) + System::String::Format(u"Primary header{0}{1}", newLine, newLine) + System::String::Format(u"Even footer{0}{1}", newLine, newLine) + System::String::Format(u"Primary footer{0}{1}", newLine, newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::PrimaryOnly:
        ASSERT_EQ(System::String::Format(u"Primary header{0}", newLine) + System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine) + System::String::Format(u"Primary footer{0}", newLine), docText);
        break;

    case Aspose::Words::Saving::TxtExportHeadersFootersMode::None:
        ASSERT_EQ(System::String::Format(u"Page 1{0}", newLine) + System::String::Format(u"Page 2{0}", newLine) + System::String::Format(u"Page 3{0}", newLine), docText);
        break;

}
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
