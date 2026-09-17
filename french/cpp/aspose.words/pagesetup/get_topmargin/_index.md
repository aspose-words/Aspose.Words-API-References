---
title: "Aspose::Words::PageSetup::get_TopMargin method"
linktitle: "get_TopMargin"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_TopMargin method. Retourne ou définit la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte du corps en C++."
type: docs
weight: 46000
url: /fr/cpp/aspose.words/pagesetup/get_topmargin/
---
## PageSetup::get_TopMargin method


Renvoie ou définit la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte principal.

```cpp
double Aspose::Words::PageSetup::get_TopMargin()
```


## Exemples



Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
