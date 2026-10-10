---
title: "Aspose::Words::Fields::FieldStyleRef::get_InsertParagraphNumberInFullContext metodo"
linktitle: "get_InsertParagraphNumberInFullContext"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldStyleRef::get_InsertParagraphNumberInFullContext metodo. Ottiene o imposta se inserire il numero del paragrafo del paragrafo di riferimento nel contesto completo in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldstyleref/get_insertparagraphnumberinfullcontext/
---
## FieldStyleRef::get_InsertParagraphNumberInFullContext method


Ottiene o imposta se inserire il numero del paragrafo del paragrafo di riferimento nel contesto completo.

```cpp
bool Aspose::Words::Fields::FieldStyleRef::get_InsertParagraphNumberInFullContext()
```


## Esempi



Mostra come utilizzare i campi STYLEREF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un elenco basato su un modello di elenco di Microsoft Word.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Questo elenco generato visualizzerà "1.a )".
// Lo spazio prima della parentesi è un carattere non delimitatore, che possiamo sopprimere.
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"\x0000" u".");
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"\x0001" u" )");

// Aggiungi testo e applica gli stili di paragrafo a cui i campi STYLEREF faranno riferimento.
builder->get_ListFormat()->set_List(list);
builder->get_ListFormat()->ListIndent();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(u"Item 2");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"List Paragraph"));
builder->Writeln(u"Item 3");
builder->get_ListFormat()->RemoveNumbers();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Inserisci un campo STYLEREF nell'intestazione e visualizza il primo testo formattato come "List Paragraph" nel documento.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");

// Inserisci un campo STYLEREF nel piè di pagina e fai visualizzare l'ultimo testo.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"List Paragraph");
field->set_SearchFromBottom(true);

builder->MoveToDocumentEnd();

// Possiamo anche usare i campi STYLEREF per fare riferimento ai numeri degli elenchi.
builder->Write(u"\nParagraph number: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumber(true);

builder->Write(u"\nParagraph number, relative context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInRelativeContext(true);

builder->Write(u"\nParagraph number, full context: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);

builder->Write(u"\nParagraph number, full context, non-delimiter chars suppressed: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldStyleRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldStyleRef, true));
field->set_StyleName(u"Quote");
field->set_InsertParagraphNumberInFullContext(true);
field->set_SuppressNonDelimiters(true);

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.STYLEREF.docx");
```

## Vedi anche

* Class [FieldStyleRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
