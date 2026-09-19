---
title: "Metodo Aspose::Words::Border::get_DistanceFromText"
linktitle: "get_DistanceFromText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Border::get_DistanceFromText. Ottiene o imposta la distanza del bordo dal testo o dal bordo della pagina in punti in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Ottiene o imposta la distanza del bordo dal testo o dal bordo della pagina in punti.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
