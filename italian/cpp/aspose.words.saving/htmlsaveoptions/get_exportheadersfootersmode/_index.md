---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode metodo"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode metodo. Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è PerSection per HTML/MHTML e None per EPUB in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è [PerSection](../../exportheadersfootersmode/) per HTML/MHTML e [None](../../exportheadersfootersmode/) per EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Note


È difficile esportare in modo significativo intestazioni e piè di pagina in HTML perché l'HTML non è paginato.

Quando questa proprietà è [PerSection](../../exportheadersfootersmode/), Aspose.Words esporta solo le intestazioni e i piè di pagina primari all'inizio e alla fine di ogni sezione.

Quando è [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) vengono esportati solo la prima intestazione primaria e l'ultimo piè di pagina primario (inclusi quelli collegati al precedente).

È possibile disabilitare completamente l'esportazione di intestazioni e piè di pagina impostando questa proprietà su [None](../../exportheadersfootersmode/).

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

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
