---
title: "Aspose::Words::ConditionalStyleCollection::ClearFormatting méthode"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting méthode. Efface tous les styles conditionnels du style de tableau en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


Efface tous les styles conditionnels du style de tableau.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## Exemples



Montre comment réinitialiser les styles de tableau conditionnels.
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

// Définissez le style de tableau pour colorer les bordures de la première ligne du tableau en rouge.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Définissez le style de tableau pour colorer les bordures de la dernière ligne du tableau en bleu.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Voici deux façons d'utiliser la méthode "ClearFormatting" pour effacer les styles conditionnels.
// 1 -  Effacez les styles conditionnels pour une partie spécifique d'un tableau:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Effacez les styles conditionnels pour l'ensemble du tableau:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## Voir aussi

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
