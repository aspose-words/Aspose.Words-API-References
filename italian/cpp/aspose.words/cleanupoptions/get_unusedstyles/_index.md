---
title: "Metodo Aspose::Words::CleanupOptions::get_UnusedStyles"
linktitle: "get_UnusedStyles"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CleanupOptions::get_UnusedStyles. Specifica se gli stili inutilizzati devono essere rimossi dal documento. Il valore predefinito è true in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/cleanupoptions/get_unusedstyles/
---
## CleanupOptions::get_UnusedStyles method


Specifica se gli stili non utilizzati devono essere rimossi dal documento. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::CleanupOptions::get_UnusedStyles() const
```


## Esempi



Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle2");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle1");
doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyParagraphStyle2");

// Combinato con gli stili predefiniti, il documento ora ha otto stili.
// Uno stile personalizzato è contrassegnato come "usato" finché c'è del testo nel documento
// formattato in quello stile. Questo significa che i 4 stili che abbiamo aggiunto sono attualmente inutilizzati.
ASSERT_EQ(8, doc->get_Styles()->get_Count());

// Applica uno stile di carattere personalizzato, e poi uno stile di elenco personalizzato. Facendo così li contrassegnerà come "usato".
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Style(doc->get_Styles()->idx_get(u"MyParagraphStyle1"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(doc->get_Styles()->idx_get(u"MyListStyle1"));
builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");

// Ora, c'è uno stile di carattere non utilizzato e uno stile di elenco non utilizzato.
// Il metodo Cleanup(), quando configurato con un oggetto CleanupOptions, può mirare agli stili non utilizzati e rimuoverli.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_UnusedLists(true);
cleanupOptions->set_UnusedStyles(true);
cleanupOptions->set_UnusedBuiltinStyles(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Rimuovere ogni nodo a cui è applicato uno stile personalizzato lo contrassegna nuovamente come "non utilizzato".
// Esegui nuovamente il metodo Cleanup per rimuoverli.
doc->get_FirstSection()->get_Body()->RemoveAllChildren();
doc->Cleanup(cleanupOptions);

ASSERT_EQ(2, doc->get_Styles()->get_Count());
```

## Vedi anche

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
