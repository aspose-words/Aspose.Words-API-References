---
title: "Aspose::Words::PageSetup::get_BorderDistanceFrom metodo"
linktitle: "get_BorderDistanceFrom"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_BorderDistanceFrom metodo. Ottiene o imposta un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/pagesetup/get_borderdistancefrom/
---
## PageSetup::get_BorderDistanceFrom method


Ottiene o imposta un valore che indica se il bordo della pagina specificato è misurato dal bordo della pagina o dal testo che lo circonda.

```cpp
Aspose::Words::PageBorderDistanceFrom Aspose::Words::PageSetup::get_BorderDistanceFrom()
```


## Esempi



Mostra come creare un bordo a banda larga e blu nella parte superiore della prima pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## Vedi anche

* Enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
