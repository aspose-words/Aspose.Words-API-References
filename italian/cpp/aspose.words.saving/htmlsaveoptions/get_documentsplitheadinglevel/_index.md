---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel. Specifica il livello massimo di intestazioni al quale dividere il documento. Il valore predefinito è %2 in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


Specifica il livello massimo di intestazioni al quale suddividere il documento. Il valore predefinito è **%2**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## Note


Quando [DocumentSplitCriteria](../get_documentsplitcriteria/) include [HeadingParagraph](../../documentsplitcriteria/) e questa proprietà è impostata a un valore da 1 a 9, il documento verrà diviso nei paragrafi formattati con gli stili **Heading 1**, **Heading 2**, **Heading 3** ecc. fino al livello di intestazione specificato.

Per impostazione predefinita, solo i paragrafi **Heading 1** e **Heading 2** provocano la divisione del documento. Impostare questa proprietà a zero impedirà al documento di essere diviso nei paragrafi di intestazione.

## Esempi



Mostra come dividere un documento HTML di output per intestazioni in più parti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ogni paragrafo che formattiamo usando uno stile "Heading" può fungere da intestazione.
// Ogni intestazione può anche avere un livello di intestazione, determinato dal numero del suo stile di intestazione.
// Le intestazioni sotto sono di livello 1-3.
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// Crea un oggetto HtmlSaveOptions e imposta il criterio di divisione su "HeadingParagraph".
// Questi criteri divideranno il documento nei paragrafi con stili "Heading" in diversi documenti più piccoli,
// e salveranno ogni documento in un file HTML separato nel file system locale.
// Imposteremo anche il livello massimo di intestazione, che divide il documento a 2.
// Salvare il documento lo dividerà alle intestazioni di livello 1 e 2, ma non a quelle da 3 a 9.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// Il nostro documento ha quattro intestazioni di livello 1 - 2. Una di queste intestazioni non sarà
// un punto di divisione poiché si trova all'inizio del documento.
// L'operazione di salvataggio dividerà il nostro documento in tre punti, creando quattro documenti più piccoli.
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
