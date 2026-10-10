---
title: "Metodo Aspose::Words::Range::UpdateFields"
linktitle: "UpdateFields"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Range::UpdateFields. Aggiorna i valori dei campi documento in questo intervallo in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Aggiorna i valori dei campi del documento in questo intervallo.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Note


Quando apri, modifichi e poi salvi un documento, Aspose.Words non aggiorna i campi automaticamente, li mantiene intatti. Pertanto, di solito vorrai chiamare questo metodo prima di salvare se hai modificato il documento programmaticamente e desideri assicurarti che i valori corretti (calcolati) dei campi compaiano nel documento salvato.

Non è necessario aggiornare i campi dopo aver eseguito un'unione di stampa perché l'unione di stampa è un tipo di aggiornamento dei campi e aggiorna automaticamente tutti i campi nel documento.

Questo metodo non aggiorna tutti i tipi di campo. Per l'elenco dettagliato dei tipi di campo supportati, consulta la Guida per gli sviluppatori.

Questo metodo non aggiorna i campi relativi agli algoritmi di layout di pagina (ad es. PAGE, PAGES, PAGEREF). I campi legati al layout di pagina vengono aggiornati quando si rende un documento o si chiama [UpdatePageLayout](../../document/updatepagelayout/).

Per aggiornare i campi nell'intero documento, usa [UpdateFields](../../document/updatefields/).

## Esempi



Mostra come aggiornare tutti i campi in un intervallo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// I campi DOCPROPERTY sopra indicati visualizzeranno il valore di questa proprietà documento integrata.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Se aggiorniamo il valore di una proprietà documento, dovremo aggiornare tutti i campi DOCPROPERTY affinché lo visualizzino.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Aggiorna tutti i campi che si trovano nell'intervallo della prima sezione.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## Vedi anche

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
