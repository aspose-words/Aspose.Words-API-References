---
title: "Aspose::Words::TabStopCollection::RemoveByIndex méthode"
linktitle: "RemoveByIndex"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStopCollection::RemoveByIndex méthode. Supprime un arrêt de tabulation à l'index spécifié de la collection en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


Supprime une tabulation à l'index spécifié de la collection.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la collection de tab stops. |

## Exemples



Montre comment sélectionner un arrêt de tabulation dans un document par son index et le supprimer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// Supprime le premier arrêt de tabulation.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## Voir aussi

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
