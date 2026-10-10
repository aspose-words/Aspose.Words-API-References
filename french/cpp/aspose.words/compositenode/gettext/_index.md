---
title: "Méthode Aspose::Words::CompositeNode::GetText"
linktitle: "GetText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::CompositeNode::GetText. Obtient le texte de ce nœud et de tous ses enfants en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/compositenode/gettext/
---
## CompositeNode::GetText method


Obtient le texte de ce nœud et de tous ses enfants.

```cpp
System::String Aspose::Words::CompositeNode::GetText() override
```

## Remarques


La chaîne retournée comprend tous les caractères de contrôle et spéciaux comme décrit dans [ControlChar](../../controlchar/).

## Exemples



Montre la différence entre l'appel des méthodes GetText et ToString sur un nœud.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText récupérera le texte visible ainsi que les codes de champ et les caractères spéciaux.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString nous donnera l'apparence du document s'il est enregistré dans le format de sauvegarde fourni.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Montre comment générer tous les paragraphes d’un document qui sont des éléments de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

for (auto&& para : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(), para->get_ListFormat()->get_ListLevel()->get_NumberStyle()) << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\"", para->GetText().Trim()) << std::endl;
}
```

## Voir aussi

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
