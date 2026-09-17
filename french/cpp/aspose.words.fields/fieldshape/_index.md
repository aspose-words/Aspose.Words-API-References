---
title: "Classe Aspose::Words::Fields::FieldShape"
linktitle: "FieldShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Fields::FieldShape. Implémente le champ SHAPE. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 93000
url: /fr/cpp/aspose.words.fields/fieldshape/
---
## FieldShape class


Implémente le champ SHAPE. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldShape : public Aspose::Words::Fields::Field
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Obtient le texte qui représente le résultat du champ affiché. |
| [get_End](../field/get_end/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldEnd](../field/get_fieldend/)() const | Obtient le nœud qui représente la fin du champ. |
| [get_FieldStart](../field/get_fieldstart/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Format](../field/get_format/)() | Obtient un objet [FieldFormat](../fieldformat/) qui fournit un accès typé au format du champ. |
| [get_IsDirty](../field/get_isdirty/)() | Obtient ou définit si le résultat actuel du champ n'est plus correct (obsolète) en raison d'autres modifications apportées au document. |
| [get_IsLocked](../field/get_islocked/)() | Obtient ou définit si le champ est verrouillé (ne doit pas recalculer son résultat). |
| [get_LocaleId](../field/get_localeid/)() | Obtient ou définit le LCID du champ. |
| [get_Result](../field/get_result/)() | Obtient ou définit le texte situé entre le séparateur du champ et la fin du champ. |
| [get_Separator](../field/get_separator/)() | Obtient le nœud qui représente le séparateur du champ. Peut être **null**. |
| [get_Start](../field/get_start/)() const | Obtient le nœud qui représente le début du champ. |
| [get_Text](./get_text/)() | Obtient ou définit le texte à récupérer. |
| virtual [get_Type](../field/get_type/)() const | Obtient le type de champ Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat des champs enfants sont inclus. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Renvoie le texte entre le début du champ et le séparateur du champ (ou la fin du champ s'il n'y a pas de séparateur). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Supprime le champ du document. Renvoie un nœud juste après le champ. Si la fin du champ est le dernier enfant de son nœud parent, renvoie le paragraphe parent. Si le champ est déjà supprimé, renvoie **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Définisseur pour [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Définisseur pour [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FieldShape::get_Text](./get_text/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Effectue le détachement du champ. |
| [Update](../field/update/)() | Effectue la mise à jour du champ. Lance une exception si le champ est déjà en cours de mise à jour. |
| [Update](../field/update/)(bool) | Effectue une mise à jour de champ. Lève une exception si le champ est déjà en cours de mise à jour. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
