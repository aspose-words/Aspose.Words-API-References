---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Level méthode"
linktitle: "get_Level"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Level méthode. Obtient le niveau auquel ce SDT apparaît dans l'arborescence du document en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_level/
---
## StructuredDocumentTag::get_Level method


Obtient le niveau auquel ce **SDT** apparaît dans l'arborescence du document.

```cpp
Aspose::Words::Markup::MarkupLevel Aspose::Words::Markup::StructuredDocumentTag::get_Level() const override
```


## Exemples



Montre comment créer une balise de document structuré dans une zone de texte simple et modifier son apparence.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez une balise de document structuré qui contiendra du texte simple.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Définissez le titre et la couleur du cadre qui apparaît lorsque vous survolez la balise de document structuré dans Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Définissez une balise pour cette balise de document structuré, qui est récupérable
// en tant qu'élément XML nommé "tag", avec la chaîne ci‑dessous dans son attribut "@val".
tag->set_Tag(u"MyPlainTextSDT");

// Chaque balise de document structuré possède un ID unique aléatoire.
ASSERT_TRUE(tag->get_Id() > 0);

// Définissez la police du texte à l'intérieur de la balise de document structuré.
tag->get_ContentsFont()->set_Name(u"Arial");

// Définissez la police du texte à la fin de la balise de document structuré.
// Tout texte que nous tapons dans le corps du document après être sortis de la balise avec les touches fléchées utilisera cette police.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// Par défaut, c'est false et appuyer sur Entrée à l'intérieur d'une balise de document structuré ne fait rien.
// Lorsqu'elle est définie sur true, notre balise de document structuré peut contenir plusieurs lignes.

// Définissez la propriété "Multiline" sur "false" pour n'autoriser que le contenu
// de cette balise de document structuré à s'étendre sur une seule ligne.
// Définissez la propriété "Multiline" sur "true" pour permettre à la balise de contenir plusieurs lignes de contenu.
tag->set_Multiline(true);

// Définissez la propriété "Appearance" sur "SdtAppearance.Tags" pour afficher des balises autour du contenu.
// Par défaut, le tag de document structuré s'affiche comme BoundingBox.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Insérez un clone de notre tag de document structuré dans un nouveau paragraphe.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Utilisez la méthode "RemoveSelfOnly" pour supprimer un tag de document structuré, tout en conservant son contenu dans le document.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## Voir aussi

* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
