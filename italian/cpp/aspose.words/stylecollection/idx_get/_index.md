---
title: "Aspose::Words::StyleCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection::idx_get metodo. Ottiene uno stile incorporato tramite il suo identificatore indipendente dalla lingua in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Restituisce uno stile incorporato per il suo identificatore indipendente dalla locale.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Un valore [StyleIdentifier](../../styleidentifier/) che specifica lo stile incorporato da recuperare. |
## Note


Quando si accede a uno stile che non esiste ancora, lo crea automaticamente.

## Esempi



Mostra come aggiungere un [Style](../../style/) alla collezione di stili di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Imposta i parametri predefiniti per i nuovi stili che potremo aggiungere successivamente a questa collezione.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Se aggiungiamo uno stile di "StyleType.Paragraph", la collezione applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Vedi anche

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Restituisce uno stile per nome o alias.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Note


Sensibile alle maiuscole/minuscole, restituisce **null** se lo stile con il nome fornito non viene trovato.

Se questo è un nome inglese di uno stile incorporato che non esiste ancora, lo crea automaticamente.

## Esempi



Mostra quando ricalcolare il layout della pagina del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Salvare un documento in PDF, in un'immagine o stamparlo per la prima volta lo farà automaticamente
// memorizzare nella cache il layout del documento all'interno delle sue pagine.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifica il documento in qualche modo.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Nella versione corrente di Aspose.Words, la modifica del documento non ricostruisce automaticamente
// il layout della pagina memorizzata nella cache. Se desideriamo che il layout memorizzato nella cache
// per rimanere aggiornato, dovremo aggiornarlo manualmente.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Vedi anche

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Restituisce uno stile per indice.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Esempi



Mostra come aggiungere un [Style](../../style/) alla collezione di stili di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Imposta i parametri predefiniti per i nuovi stili che potremo aggiungere successivamente a questa collezione.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Se aggiungiamo uno stile di "StyleType.Paragraph", la collezione applicherà i valori di
// la sua proprietà "DefaultParagraphFormat" alla proprietà "ParagraphFormat" dello stile.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Aggiungi uno stile, quindi verifica che abbia le impostazioni predefinite.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Vedi anche

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
