---
title: "Méthode Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision"
linktitle: "get_IsMoveToRevision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision. Retourne true si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé en C++."
type: docs
weight: 34000
url: /fr/cpp/aspose.words.drawing/shapebase/get_ismovetorevision/
---
## ShapeBase::get_IsMoveToRevision method


Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision()
```


## Exemples



Montre comment identifier les formes de révision de déplacement.
```cpp
// Une révision de déplacement se produit lorsque nous déplaçons un élément dans le corps du document en le découpant‑collant dans Microsoft Word tout en
// suivi des modifications. Si nous impliquons une forme en ligne dans un tel déplacement de texte, cette forme sera également une révision.
// Copier‑coller ou déplacer des formes flottantes ne crée pas de révisions de déplacement.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Les révisions de déplacement se composent de paires de révisions "Move from" et "Move to". Nous avons déplacé dans ce document une forme,
// mais tant que nous n’acceptons pas ou ne rejetons pas la révision de déplacement, il y aura deux instances de cette forme.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Ceci est la révision "Move to", qui est la forme à son lieu d’arrivée.
// Si nous acceptons la révision, cette forme de révision "Move to" disparaîtra,
// et la forme de révision "Move from" restera.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Ceci est la révision "Move from", qui est la forme à son emplacement d’origine.
// Si nous acceptons la révision, cette forme de révision "Move from" disparaîtra,
// et la forme de révision "Move to" restera.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
