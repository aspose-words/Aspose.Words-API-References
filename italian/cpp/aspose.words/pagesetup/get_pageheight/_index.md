---
title: "Metodo Aspose::Words::PageSetup::get_PageHeight"
linktitle: "get_PageHeight"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_PageHeight. Restituisce o imposta l'altezza della pagina in punti in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Restituisce o imposta l'altezza della pagina in punti.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


## Esempi



Mostra come inserire un'immagine e usarla come filigrana.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Posiziona l'immagine al centro della pagina.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## Vedi anche

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
