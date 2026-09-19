---
title: "Metodo Aspose::Words::PageSetup::get_HeaderDistance"
linktitle: "get_HeaderDistance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_HeaderDistance. Restituisce o imposta la distanza (in punti) tra l'intestazione e la parte superiore della pagina in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/pagesetup/get_headerdistance/
---
## PageSetup::get_HeaderDistance method


Restituisce o imposta la distanza (in punti) tra l'intestazione e la parte superiore della pagina.

```cpp
double Aspose::Words::PageSetup::get_HeaderDistance()
```


## Esempi



Mostra come regolare le dimensioni della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.
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

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
