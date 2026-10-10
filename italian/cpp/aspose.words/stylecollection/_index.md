---
title: "Aspose::Words::StyleCollection classe"
linktitle: "StyleCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection classe. Una collezione di oggetti Style che rappresentano sia gli stili predefiniti sia quelli definiti dall'utente in un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 65000
url: /it/cpp/aspose.words/stylecollection/
---
## StyleCollection class


Una collezione di oggetti [Style](../style/) che rappresentano sia gli stili predefiniti sia quelli definiti dall'utente in un documento. Per saperne di più, visita l'articolo di documentazione [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Crea un nuovo stile definito dall'utente e lo aggiunge alla raccolta. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Copia uno stile in questa raccolta. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Rimuove tutti gli stili dal pannello Quick [Style](../style/) Gallery. |
| [get_Count](./get_count/)() | Restituisce il numero di stili nella raccolta. |
| [get_DefaultFont](./get_defaultfont/)() | Restituisce la formattazione predefinita del testo del documento. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Restituisce la formattazione predefinita del paragrafo del documento. |
| [get_Document](./get_document/)() const | Restituisce il documento proprietario. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che elencherà gli stili in ordine alfabetico dei loro nomi. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Restituisce uno stile per nome o alias. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Restituisce uno stile incorporato per il suo identificatore indipendente dalla locale. |
| [idx_get](./idx_get/)(int32_t) | Restituisce uno stile per indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea uno stile di paragrafo personalizzato.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea un elenco e assicurati che i paragrafi che usano questo stile lo utilizzino.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Applica lo stile di paragrafo al paragrafo corrente del document builder, quindi aggiungi del testo.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifica lo stile del DocumentBuilder in uno che non abbia formattazione di elenco e scrivi un altro paragrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
