---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath méthode"
linktitle: "get_ConvertShapeToOfficeMath"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath méthode. Obtient ou définit si les formes avec EquationXML doivent être converties en objets Office Math en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.loading/loadoptions/get_convertshapetoofficemath/
---
## LoadOptions::get_ConvertShapeToOfficeMath method


Obtient ou définit si les formes avec EquationXML doivent être converties en objets Office [Math](../../../aspose.words.math/) .

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath() const
```


## Exemples



Montre comment convertir les formes EquationXML en objets Office [Math](../../../aspose.words.math/) .
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

// Utilisez ce drapeau pour spécifier si les formes avec des attributs EquationXML doivent être converties
// en objets Office Math puis charger le document.
loadOptions->set_ConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    ASSERT_EQ(16, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
    ASSERT_EQ(34, doc->GetChildNodes(Aspose::Words::NodeType::OfficeMath, true)->get_Count());
}
else
{
    ASSERT_EQ(24, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
    ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::OfficeMath, true)->get_Count());
}
```

## Voir aussi

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
