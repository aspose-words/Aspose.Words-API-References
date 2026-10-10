---
title: "Metodo Aspose::Words::ParagraphFormat::get_StyleIdentifier"
linktitle: "get_StyleIdentifier"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_StyleIdentifier. Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile di paragrafo applicato a questa formattazione in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words/paragraphformat/get_styleidentifier/
---
## ParagraphFormat::get_StyleIdentifier method


Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile di paragrafo applicato a questa formattazione.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::ParagraphFormat::get_StyleIdentifier()
```


## Esempi



Mostra come inserire un indice (TOC) in un documento utilizzando gli stili di intestazione come voci.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un indice per la prima pagina del documento.
// Configura l'indice per includere i paragrafi con intestazioni di livello da 1 a 3.
// Inoltre, imposta le sue voci come collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il tasto sinistro in Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Popola l'indice aggiungendo paragrafi con stili di intestazione.
// Ogni intestazione di questo tipo con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Un indice è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## Vedi anche

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
