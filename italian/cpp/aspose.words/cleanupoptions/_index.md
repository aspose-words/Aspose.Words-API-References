---
title: "Classe Aspose::Words::CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::CleanupOptions. Consente di specificare le opzioni per la pulizia del documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/cleanupoptions/
---
## CleanupOptions class


Consente di specificare le opzioni per la pulizia del documento. Per saperne di più, visita l'articolo di documentazione [Clean Up a Document](https://docs.aspose.com/words/cpp/clean-up-a-document/).

```cpp
class CleanupOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [CleanupOptions](./cleanupoptions/)() |  |
| [get_DuplicateStyle](./get_duplicatestyle/)() const | Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è **false**. |
| [get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/)() const | Specifica che gli stili non utilizzati [BuiltIn](../style/get_builtin/) devono essere rimossi dal documento. |
| [get_UnusedLists](./get_unusedlists/)() const | Specifica se le liste non utilizzate e le definizioni di lista devono essere rimosse dal documento. Il valore predefinito è **true**. |
| [get_UnusedStyles](./get_unusedstyles/)() const | Specifica se gli stili non utilizzati devono essere rimossi dal documento. Il valore predefinito è **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DuplicateStyle](./set_duplicatestyle/)(bool) | Metodo setter per [Aspose::Words::CleanupOptions::get_DuplicateStyle](./get_duplicatestyle/). |
| [set_UnusedBuiltinStyles](./set_unusedbuiltinstyles/)(bool) | Metodo setter per [Aspose::Words::CleanupOptions::get_UnusedBuiltinStyles](./get_unusedbuiltinstyles/). |
| [set_UnusedLists](./set_unusedlists/)(bool) | Metodo setter per [Aspose::Words::CleanupOptions::get_UnusedLists](./get_unusedlists/). |
| [set_UnusedStyles](./set_unusedstyles/)(bool) | Metodo setter per [Aspose::Words::CleanupOptions::get_UnusedStyles](./get_unusedstyles/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
