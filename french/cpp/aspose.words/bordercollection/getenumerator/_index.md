---
title: "Aspose::Words::BorderCollection::GetEnumerator méthode"
linktitle: "GetEnumerator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::BorderCollection::GetEnumerator. Retourne un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les bordures de la collection.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Exemples



Montre comment parcourir et modifier toutes les bordures d'un objet de format de paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configurez les paramètres de format de paragraphe du constructeur pour créer une bordure ondulée verte sur tous les côtés.
System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> enumerator = borders->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Border> border = enumerator->get_Current();
        border->set_Color(System::Drawing::Color::get_Green());
        border->set_LineStyle(Aspose::Words::LineStyle::Wave);
        border->set_LineWidth(3);
    }
}

// Insérez un paragraphe. Nos paramètres de bordure détermineront l'apparence de sa bordure.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## Voir aussi

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
