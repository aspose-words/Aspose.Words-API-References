---
title: "Aspose::Words::Style::get_ListFormat méthode"
linktitle: "get_ListFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Style::get_ListFormat méthode. Fournit l'accès aux propriétés de formatage de liste d'un style de paragraphe en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/style/get_listformat/
---
## Style::get_ListFormat method


Fournit l’accès aux propriétés de formatage de liste d’un style de paragraphe.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Style::get_ListFormat()
```

## Remarques


Cette propriété n'est valable que pour les styles de paragraphe. Pour les autres types de style, cette propriété renvoie **null**.

## Exemples



Montre comment créer et utiliser un style de paragraphe avec un formatage de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un style de paragraphe personnalisé.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Créez une liste et assurez-vous que les paragraphes qui utilisent ce style utiliseront cette liste.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Appliquez le style de paragraphe au paragraphe actuel du constructeur de document, puis ajoutez du texte.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifiez le style du DocumentBuilder pour qu'il n'ait aucun format de liste et écrivez un autre paragraphe.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Voir aussi

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
