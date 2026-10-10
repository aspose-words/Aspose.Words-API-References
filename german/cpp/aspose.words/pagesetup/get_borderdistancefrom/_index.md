---
title: "Aspose::Words::PageSetup::get_BorderDistanceFrom Methode"
linktitle: "get_BorderDistanceFrom"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_BorderDistanceFrom Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umschlossenen Text gemessen wird in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/pagesetup/get_borderdistancefrom/
---
## PageSetup::get_BorderDistanceFrom method


Liest oder legt einen Wert fest, der angibt, ob der angegebene Seitenrand vom Rand der Seite oder vom umschlossenen Text gemessen wird.

```cpp
Aspose::Words::PageBorderDistanceFrom Aspose::Words::PageSetup::get_BorderDistanceFrom()
```


## Beispiele



Zeigt, wie man einen breiten blauen Rahmen am oberen Rand der ersten Seite erstellt.
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

## Siehe auch

* Enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
