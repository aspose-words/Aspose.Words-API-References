---
title: "Aspose::Words::Document::UpdateFields metodo"
linktitle: "UpdateFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::UpdateFields metodo. Aggiorna i valori dei campi in tutto il documento in C++."
type: docs
weight: 96000
url: /it/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Aggiorna i valori dei campi in tutto il documento.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Note


Quando apri, modifichi e poi salvi un documento, Aspose.Words non aggiorna i campi automaticamente, li mantiene intatti. Pertanto, di solito vorrai chiamare questo metodo prima di salvare se hai modificato il documento programmaticamente e desideri assicurarti che i valori corretti (calcolati) dei campi compaiano nel documento salvato.

Non è necessario aggiornare i campi dopo aver eseguito un'unione di stampa perché l'unione di stampa è un tipo di aggiornamento dei campi e aggiorna automaticamente tutti i campi nel documento.

Questo metodo non aggiorna tutti i tipi di campo. Per l'elenco dettagliato dei tipi di campo supportati, consulta la Guida per gli sviluppatori.

Questo metodo non aggiorna i campi relativi agli algoritmi di impaginazione (ad es. PAGE, PAGES, PAGEREF). I campi legati all'impaginazione vengono aggiornati quando si rende un documento o si chiama [UpdatePageLayout](../updatepagelayout/).

Utilizza il metodo [NormalizeFieldTypes](../normalizefieldtypes/) prima di aggiornare i campi se ci sono state modifiche al documento che hanno influenzato i tipi di campo.

Per aggiornare i campi in una parte specifica del documento, utilizza [UpdateFields](../../range/updatefields/).

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


Mostra come usare il campo QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un campo QUOTE, che visualizzerà il valore della sua proprietà Text.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Inserisci un campo QUOTE e annida un campo DATE al suo interno.
// I campi DATE aggiornano il loro valore alla data corrente ogni volta che apriamo il documento con Microsoft Word.
// Annidare il campo DATE all'interno del campo QUOTE in questo modo bloccherà il suo valore
// alla data in cui abbiamo creato il documento.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Aggiorna tutti i campi per visualizzare i risultati corretti.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Mostra come impostare i dettagli dell'utente e visualizzarli usando i campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un oggetto UserInformation e impostalo come origine dati per i campi che visualizzano le informazioni dell'utente.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// Inserisci i campi USERNAME, USERINITIALS e USERADDRESS, che visualizzano i valori di
// le rispettive proprietà dell'oggetto UserInformation che abbiamo creato sopra.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// L'oggetto field options ha anche un utente predefinito statico a cui i campi di tutti i documenti possono fare riferimento.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
