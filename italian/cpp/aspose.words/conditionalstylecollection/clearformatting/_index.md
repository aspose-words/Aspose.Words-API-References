---
title: "Metodo Aspose::Words::ConditionalStyleCollection::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting method. Cancella tutti gli stili condizionali dello stile tabella in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


Cancella tutti gli stili condizionali dello stile di tabella.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## Esempi



Mostra come ripristinare gli stili condizionali delle tabelle.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// Imposta lo stile della tabella per colorare i bordi della prima riga della tabella in rosso.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Imposta lo stile della tabella per colorare i bordi dell'ultima riga della tabella in blu.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Di seguito sono riportati due modi per utilizzare il metodo "ClearFormatting" per cancellare gli stili condizionali.
// 1 -  Cancella gli stili condizionali per una parte specifica di una tabella:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Cancella gli stili condizionali per l'intera tabella:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## Vedi anche

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
