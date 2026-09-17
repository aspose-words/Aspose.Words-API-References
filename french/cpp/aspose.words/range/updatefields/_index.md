---
title: "Méthode Aspose::Words::Range::UpdateFields"
linktitle: "UpdateFields"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Range::UpdateFields. Met à jour les valeurs des champs du document dans cette plage en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Met à jour les valeurs des champs du document dans cette plage.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Remarques


Lorsque vous ouvrez, modifiez puis enregistrez un document, Aspose.Words ne met pas à jour les champs automatiquement, il les conserve intacts. Par conséquent, vous souhaiterez généralement appeler cette méthode avant d'enregistrer si vous avez modifié le document de manière programmatique et souhaitez vous assurer que les valeurs de champ appropriées (calculées) apparaissent dans le document enregistré.

Il n'est pas nécessaire de mettre à jour les champs après l'exécution d'une fusion de courrier car la fusion de courrier est une forme de mise à jour des champs et met automatiquement à jour tous les champs du document.

Cette méthode ne met pas à jour tous les types de champs. Pour la liste détaillée des types de champs pris en charge, consultez le Guide du programmeur.

Cette méthode ne met pas à jour les champs liés aux algorithmes de mise en page (par ex. PAGE, PAGES, PAGEREF). Les champs liés à la mise en page sont mis à jour lorsque vous rendez un document ou appelez [UpdatePageLayout](../../document/updatepagelayout/).

Pour mettre à jour les champs dans l'ensemble du document, utilisez [UpdateFields](../../document/updatefields/).

## Exemples



Montre comment mettre à jour tous les champs dans une plage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// Les champs DOCPROPERTY ci‑dessus afficheront la valeur de cette propriété de document intégrée.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Si nous mettons à jour la valeur d'une propriété de document, nous devrons mettre à jour tous les champs DOCPROPERTY pour l'afficher.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Mettez à jour tous les champs qui se trouvent dans la plage de la première section.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## Voir aussi

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
