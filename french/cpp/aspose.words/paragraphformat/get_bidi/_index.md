---
title: "Aspose::Words::ParagraphFormat::get_Bidi méthode"
linktitle: "get_Bidi"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_Bidi méthode. Obtient ou définit si ce paragraphe est de droite à gauche en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/paragraphformat/get_bidi/
---
## ParagraphFormat::get_Bidi method


Obtient ou définit si ce paragraphe est de droite à gauche.

```cpp
bool Aspose::Words::ParagraphFormat::get_Bidi()
```

## Remarques


Lorsque **true**, les runs et autres objets en ligne dans ce paragraphe sont disposés de droite à gauche.

## Exemples



Montre comment créer des listes compatibles avec les langues de droite à gauche à l'aide des champs BIDIOUTLINE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le champ BIDIOUTLINE numérote les paragraphes comme les champs AUTONUM/LISTNUM,
// mais n'est visible que lorsqu'une langue d'édition de droite à gauche est activée, comme l'hébreu ou l'arabe.
// Le champ suivant affichera ".1", l'équivalent RTL du numéro de liste "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Ajoutez deux champs BIDIOUTLINE supplémentaires, qui afficheront ".2" et ".3".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Définissez l'alignement horizontal du texte pour chaque paragraphe du document sur RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Si nous activons une langue d'édition de droite à gauche dans Microsoft Word, nos champs afficheront des nombres.
// Sinon, ils afficheront "###".
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Montre comment détecter la direction du texte d'un document texte brut.
```cpp
// Créez un objet "TxtLoadOptions", que nous pouvons passer au constructeur d'un document
// pour modifier la façon dont nous chargeons un document texte brut.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Définissez la propriété "DocumentDirection" sur "DocumentDirection.Auto" détecte automatiquement
// la direction de chaque paragraphe de texte que Aspose.Words charge à partir d'un texte brut.
// La propriété "Bidi" de chaque paragraphe stockera sa direction.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Détecter le texte hébreu comme de droite à gauche.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Détecter le texte anglais comme de droite à gauche.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
