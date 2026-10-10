---
title: "Aspose::Words::ConditionalStyleCollection::ClearFormatting‑metod"
linktitle: "ClearFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting‑metod. Rensar alla villkorliga stilar för tabellstilen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


Rensar alla villkorliga stilar i tabellstilen.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## Exempel



Visar hur man återställer villkorliga tabellformat.
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

// Ställ in tabellformatet för att färga kanterna på den första raden i tabellen röd.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Ställ in tabellformatet för att färga kanterna på den sista raden i tabellen blå.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Nedan följer två sätt att använda metoden "ClearFormatting" för att rensa de villkorliga stilarna.
// 1 -  Rensa de villkorliga stilarna för en specifik del av en tabell:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Rensa de villkorliga stilarna för hela tabellen:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## Se även

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
