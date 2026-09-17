---
title: "Méthode Aspose::Words::Drawing::Charts::Chart::get_SourceFullName"
linktitle: "get_SourceFullName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Charts::Chart::get_SourceFullName. Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Obtient le chemin et le nom d'un fichier xls/xlsx auquel ce graphique est lié.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Exemples



Montre comment obtenir/definir le nom complet du document xls/xlsx externe si le graphique est lié.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## Voir aussi

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
