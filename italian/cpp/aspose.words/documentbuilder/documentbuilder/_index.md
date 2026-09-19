---
title: "Aspose::Words::DocumentBuilder::DocumentBuilder costruttore"
linktitle: "DocumentBuilder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::DocumentBuilder costruttore. Inizializza una nuova istanza di questa classe in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder::DocumentBuilder() constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder()
```


## Esempi



Mostra come inserire testo formattato usando [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specifica la formattazione del carattere, poi aggiungi il testo.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&) constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | L'oggetto [Document](../../document/) a cui collegare. |

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

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | L'oggetto [Document](../../document/) a cui collegare. |
| opzioni | const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\& | Opzioni aggiuntive per il processo di costruzione del documento. |

## Esempi



Mostra come ignorare la formattazione della tabella per il contenuto successivo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Aggiunge contenuto prima della tabella.
// La dimensione predefinita del carattere è 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Modifica la dimensione del carattere all'interno della tabella.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Se ContextTableFormatting è vero, la formattazione della tabella non viene applicata al contenuto successivo.
// Se ContextTableFormatting è falso, la formattazione della tabella viene applicata al contenuto successivo.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Vedi anche

* Class [Document](../../document/)
* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


Inizializza una nuova istanza di questa classe.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


## Esempi



Mostra come ignorare la formattazione della tabella per il contenuto successivo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Aggiunge contenuto prima della tabella.
// La dimensione predefinita del carattere è 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Modifica la dimensione del carattere all'interno della tabella.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Se ContextTableFormatting è vero, la formattazione della tabella non viene applicata al contenuto successivo.
// Se ContextTableFormatting è falso, la formattazione della tabella viene applicata al contenuto successivo.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Vedi anche

* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
