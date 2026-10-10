---
title: "Enum Aspose::Words::Saving::ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Saving::ExportHeadersFootersMode. Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB in C++."
type: docs
weight: 55000
url: /it/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Intestazioni e piè di pagina non vengono esportati. |
| PerSection | 1 | Le intestazioni e i piè di pagina primari vengono esportati all'inizio e alla fine di ogni sezione. |
| FirstSectionHeaderLastSectionFooter | 2 | L'intestazione primaria della prima sezione viene esportata all'inizio del documento e il piè di pagina primario alla fine. |
| FirstPageHeaderFooterPerSection | 3 | L'intestazione e il piè di pagina della prima pagina vengono esportati all'inizio e alla fine di ogni sezione. |


## Esempi



Mostra come omettere intestazioni/piè di pagina quando si salva un documento in HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Questo documento contiene intestazioni e piè di pagina. Possiamo accedervi tramite la collezione "HeadersFooters".
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Formati come .html non suddividono il documento in pagine, quindi intestazioni/piè di pagina non funzioneranno allo stesso modo.
// come farebbero quando apriamo il documento come .docx usando Microsoft Word.
// Se convertiamo un documento con intestazioni/piè di pagina in html, la conversione assimilerà le intestazioni/piè di pagina nel testo del corpo.
// Possiamo usare un oggetto SaveOptions per omettere intestazioni/piè di pagina durante la conversione in html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Apri il nostro documento salvato e verifica che non contenga il testo dell'intestazione.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
