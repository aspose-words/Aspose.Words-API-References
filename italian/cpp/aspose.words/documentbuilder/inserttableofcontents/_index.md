---
title: "Metodo Aspose::Words::DocumentBuilder::InsertTableOfContents"
linktitle: "InsertTableOfContents"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertTableOfContents. Inserisce un campo TOC (indice) nel documento in C++."
type: docs
weight: 48000
url: /it/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


Inserisce un campo TOC (indice) nel documento.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| interruttori | const System::String\& | Gli interruttori del campo TOC. |
## Note


Questo metodo inserisce un campo TOC (indice) nel documento nella posizione corrente.

Un indice in un documento Word può essere creato in diversi modi e formattato usando una varietà di opzioni. Il modo in cui l'indice è costruito e visualizzato da Microsoft Word è controllato dagli interruttori del campo.

La maniera più semplice per specificare gli interruttori è inserire e configurare un indice in un documento Word usando il menu Inserisci->Riferimento->Indice e il menu [Tables](../../../aspose.words.tables/), quindi attivare la visualizzazione dei codici campo per vedere gli interruttori. È possibile premere Alt+F9 in Microsoft Word per attivare o disattivare la visualizzazione dei codici campo.

Ad esempio, dopo aver creato un indice, il seguente campo viene inserito nel documento: **%{ TOC \o "1-3" \h \z }**. È possibile copiare **%\o "1-3" \h \z** e usarlo come parametro degli interruttori.

Nota che [InsertTableOfContents()](../) inserirà solo un campo TOC, ma non costruirà effettivamente l'indice. L'indice viene costruito da Microsoft Word quando il campo viene aggiornato.

Se inserisci un indice usando questo metodo e poi apri il file in Microsoft Word, non vedrai l'indice perché il campo TOC non è ancora stato aggiornato.

In Microsoft Word, i campi non vengono aggiornati automaticamente all'apertura di un documento, ma è possibile aggiornare i campi in un documento in qualsiasi momento premendo F9.

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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
