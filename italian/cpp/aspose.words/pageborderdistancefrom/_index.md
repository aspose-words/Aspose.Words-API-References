---
title: "Aspose::Words::PageBorderDistanceFrom enum"
linktitle: "PageBorderDistanceFrom"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageBorderDistanceFrom enum. Specifica il posizionamento del bordo della pagina rispetto al margine della pagina in C++."
type: docs
weight: 107000
url: /it/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Specifica la posizione del bordo della pagina rispetto al margine della pagina.

```cpp
enum class PageBorderDistanceFrom
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Text | 0 | La posizione di [Bordo](../border/) è misurata dal margine della pagina. |
| PageEdge | 1 | La posizione di [Bordo](../border/) è misurata dal bordo della pagina. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
