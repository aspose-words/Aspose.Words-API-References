---
title: "Aspose::Words::HeaderFooter::HeaderFooter constructeur"
linktitle: "HeaderFooter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::HeaderFooter::HeaderFooter constructeur. Crée un nouvel en-tête ou pied de page du type spécifié en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


Crée un nouvel en-tête ou pied de page du type spécifié.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
| headerFooterType | Aspose::Words::HeaderFooterType | Une valeur [HeaderFooterType](../get_headerfootertype/) qui spécifie le type de l'en-tête ou du pied de page. |
## Remarques


Lorsque [HeaderFooter](../) est créé, il appartient au document spécifié, mais n'est pas encore intégré au document et [ParentNode](../../node/get_parentnode/) est **null**.

Pour ajouter [HeaderFooter](../) à une [Section](../../section/) utilisez [InsertAfter1()</see>, <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../), ou la propriété [HeadersFooters](../../section/get_headersfooters/) et les méthodes [Add()](../), [Insert()](../).

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

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
