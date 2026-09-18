---
title: "Aspose::Words::Saving::ExportHeadersFootersMode enum"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ExportHeadersFootersMode enum. Gibt an, wie Kopf- und Fußzeilen zu HTML, MHTML oder EPUB in C++ exportiert werden."
type: docs
weight: 55000
url: /de/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Gibt an, wie Kopf‑ und Fußzeilen nach HTML, MHTML oder EPUB exportiert werden.

```cpp
enum class ExportHeadersFootersMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Kopf- und Fußzeilen werden nicht exportiert. |
| PerSection | 1 | Primäre Kopf- und Fußzeilen werden am Anfang und Ende jedes Abschnitts exportiert. |
| FirstSectionHeaderLastSectionFooter | 2 | Die primäre Kopfzeile des ersten Abschnitts wird am Anfang des Dokuments exportiert und die primäre Fußzeile am Ende. |
| FirstPageHeaderFooterPerSection | 3 | Kopf- und Fußzeile der ersten Seite werden am Anfang und Ende jedes Abschnitts exportiert. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
