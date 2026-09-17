---
title: "Aspose::Words::Fields::FieldShape::get_Text méthode"
linktitle: "get_Text"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldShape::get_Text méthode. Obtient ou définit le texte à récupérer en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Obtient ou définit le texte à récupérer.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


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


Montre comment certains champs plus anciens de Microsoft Word tels que SHAPE et EMBED sont gérés lors du chargement.
```cpp
// Ouvrez un document qui a été créé dans Microsoft Word 2003.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Si nous ouvrons le document Word et appuyons sur Alt+F9, nous verrons un champ SHAPE et un champ EMBED.
// Un champ SHAPE est l'ancre/la toile pour un objet AutoShape avec le style de retour à la ligne « En ligne avec le texte » activé.
// Un champ EMBED a la même fonction, mais pour un objet incorporé,
// tel qu'une feuille de calcul provenant d'un document Excel externe.
// Cependant, ces champs n'apparaîtront pas dans la collection Fields du document.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Ces champs ne sont pris en charge que par les anciennes versions de Microsoft Word.
// Le processus de chargement du document convertira ces champs en objets Shape,
// que nous pouvons accéder dans la collection de nœuds du document.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// Le premier nœud Shape correspond au champ SHAPE dans le document d'entrée,
// qui est la toile en ligne pour l'AutoShape.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// Le deuxième nœud Shape est l'AutoShape lui‑même.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Le troisième Shape est ce qui était le champ EMBED contenant la feuille de calcul externe.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## Voir aussi

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
