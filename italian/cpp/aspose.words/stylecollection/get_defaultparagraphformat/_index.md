---
title: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat metodo"
linktitle: "get_DefaultParagraphFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat metodo. Ottiene la formattazione del paragrafo predefinita del documento in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/stylecollection/get_defaultparagraphformat/
---
## StyleCollection::get_DefaultParagraphFormat method


Restituisce la formattazione predefinita del paragrafo del documento.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::StyleCollection::get_DefaultParagraphFormat()
```

## Note


Nota che le impostazioni predefinite a livello di documento sono state introdotte in Microsoft Word 2007 e sono supportate completamente solo nei formati OOXML ([Docx](../../loadformat/)). I formati di documento precedenti non supportano la formattazione del paragrafo predefinita del documento.

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

* Class [ParagraphFormat](../../paragraphformat/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
