---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex méthode"
linktitle: "GetPositionByIndex"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex méthode. Obtient la position (en points) du tab stop à l'index spécifié en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Obtient la position (en points) de la tabulation à l'index spécifié.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la collection de tab stops. |

### ReturnValue

La position du tab stop.

## Exemples



Montre comment trouver un tab stop par son index et vérifier sa position.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Vérifiez la position du deuxième tab stop dans la collection.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## Voir aussi

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
