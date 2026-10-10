---
title: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat méthode"
linktitle: "get_DefaultParagraphFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat méthode. Obtient le formatage de paragraphe par défaut du document en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/stylecollection/get_defaultparagraphformat/
---
## StyleCollection::get_DefaultParagraphFormat method


Obtient le formatage de paragraphe par défaut du document.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::StyleCollection::get_DefaultParagraphFormat()
```

## Remarques


Notez que les paramètres par défaut à l’échelle du document ont été introduits dans Microsoft Word 2007 et ne sont entièrement pris en charge que dans les formats OOXML ([Docx](../../loadformat/)). Les formats de document antérieurs ne prennent pas en charge le formatage de paragraphe par défaut du document.

## Exemples



Montre comment ajouter un [Style](../../style/) à la collection de styles d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Définissez les paramètres par défaut pour les nouveaux styles que nous pourrons ajouter ultérieurement à cette collection.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si nous ajoutons un style de "StyleType.Paragraph", la collection appliquera les valeurs de
// sa propriété "DefaultParagraphFormat" à la propriété "ParagraphFormat" du style.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Ajoutez un style, puis vérifiez qu’il possède les paramètres par défaut.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Voir aussi

* Class [ParagraphFormat](../../paragraphformat/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
