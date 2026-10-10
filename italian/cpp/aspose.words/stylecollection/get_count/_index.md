---
title: "Aspose::Words::StyleCollection::get_Count metodo"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::StyleCollection::get_Count metodo. Ottiene il numero di stili nella collezione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/stylecollection/get_count/
---
## StyleCollection::get_Count method


Restituisce il numero di stili nella raccolta.

```cpp
int32_t Aspose::Words::StyleCollection::get_Count()
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

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
