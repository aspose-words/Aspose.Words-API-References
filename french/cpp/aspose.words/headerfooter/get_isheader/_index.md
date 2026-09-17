---
title: "Aspose::Words::HeaderFooter::get_IsHeader méthode"
linktitle: "get_IsHeader"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::HeaderFooter::get_IsHeader méthode. True si cet objet HeaderFooter est un en-tête en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/headerfooter/get_isheader/
---
## HeaderFooter::get_IsHeader method


True si cet objet [HeaderFooter](../) est un en-tête.

```cpp
bool Aspose::Words::HeaderFooter::get_IsHeader()
```


## Exemples



Montre comment créer un en-tête et un pied de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez un en-tête et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra en haut de chaque page de cette section, au-dessus du texte principal.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Créez un pied de page et ajoutez-y un paragraphe. Le texte de ce paragraphe
// apparaîtra en bas de chaque page de cette section, sous le texte principal.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

## Voir aussi

* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
