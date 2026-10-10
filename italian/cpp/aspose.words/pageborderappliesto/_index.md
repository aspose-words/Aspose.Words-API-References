---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageBorderAppliesTo enum. Specifica su quali pagine il bordo della pagina viene stampato in C++."
type: docs
weight: 106000
url: /it/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Specifica su quali pagine il bordo della pagina viene stampato.

```cpp
enum class PageBorderAppliesTo
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AllPages | 0 | Il bordo della pagina è mostrato su tutte le pagine della sezione. |
| FirstPage | 1 | Il bordo della pagina è mostrato solo sulla prima pagina della sezione. |
| OtherPages | 2 | Il bordo della pagina è mostrato su tutte le pagine tranne la prima pagina della sezione. |


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
