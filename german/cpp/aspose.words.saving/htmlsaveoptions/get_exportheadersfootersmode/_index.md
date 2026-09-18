---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode Methode"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode Methode. Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB ausgegeben werden. Der Standardwert ist PerSection für HTML/MHTML und None für EPUB in C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB ausgegeben werden. Der Standardwert ist [PerSection](../../exportheadersfootersmode/) für HTML/MHTML und [None](../../exportheadersfootersmode/) für EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Hinweise


Es ist schwierig, Kopf- und Fußzeilen sinnvoll in HTML auszugeben, weil HTML nicht paginiert ist.

Wenn diese Eigenschaft [PerSection](../../exportheadersfootersmode/) ist, exportiert Aspose.Words nur primäre Kopf- und Fußzeilen am Anfang und Ende jedes Abschnitts.

Wenn sie [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) ist, werden nur die erste primäre Kopfzeile und die letzte primäre Fußzeile (einschließlich Verknüpfung zur vorherigen) exportiert.

Sie können den Export von Kopf- und Fußzeilen vollständig deaktivieren, indem Sie diese Eigenschaft auf [None](../../exportheadersfootersmode/) setzen.

## Beispiele



Zeigt, wie Kopf‑/Fußzeilen beim Speichern eines Dokuments als HTML weggelassen werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Dieses Dokument enthält Kopf‑ und Fußzeilen. Wir können über die "HeadersFooters"‑Sammlung darauf zugreifen.
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Formate wie .html teilen das Dokument nicht in Seiten, sodass Kopf‑/Fußzeilen nicht auf dieselbe Weise funktionieren.
// wie sie es tun würden, wenn wir das Dokument als .docx mit Microsoft Word öffnen.
// Wenn wir ein Dokument mit Kopf‑/Fußzeilen in HTML konvertieren, wird die Konvertierung die Kopf‑/Fußzeilen in den Fließtext übernehmen.
// Wir können ein SaveOptions‑Objekt verwenden, um Kopf‑/Fußzeilen beim Konvertieren zu HTML wegzulassen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Öffnen Sie unser gespeichertes Dokument und prüfen Sie, dass es den Text der Kopfzeile nicht enthält.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## Siehe auch

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
