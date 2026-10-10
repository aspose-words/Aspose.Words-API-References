---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition méthode"
linktitle: "GetIndexByPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition méthode. Obtient l'index d'un tab stop avec la position spécifiée en points en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Obtient l'index d'une tabulation avec la position spécifiée en points.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Exemples



Montre comment rechercher une position pour voir si un tab stop existe à cet endroit et obtenir son index.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Ajoutez un tab stop à une position de 30 mm.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Un résultat de "0" retourné par "GetIndexByPosition" confirme qu'un tab stop
// à 30 mm existe dans cette collection, et il est à l'index 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// Un "-1" retourné par "GetIndexByPosition" confirme que
// il n'y a aucun tab stop dans cette collection avec une position de 60 mm.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## Voir aussi

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
