---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. Specifica a cosa è relativo il posizionamento orizzontale di una forma o di un riquadro di testo in C++."
type: docs
weight: 33000
url: /it/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Specifica rispetto a cosa è relativa la posizione orizzontale di una forma o di un riquadro di testo.

```cpp
enum class RelativeHorizontalPosition
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Margine | 0 | Specifica che il posizionamento orizzontale deve essere relativo ai margini della pagina. |
| Page | 1 | L'oggetto è posizionato rispetto al bordo sinistro della pagina. |
| Colonna | 2 | L'oggetto è posizionato rispetto al lato sinistro della colonna. |
| Character | 3 | L'oggetto è posizionato rispetto al lato sinistro del paragrafo. |
| LeftMargin | 4 | Specifica che il posizionamento orizzontale deve essere relativo al margine sinistro della pagina. |
| RightMargin | 5 | Specifica che il posizionamento orizzontale deve essere relativo al margine destro della pagina. |
| InsideMargin | 6 | Specifica che il posizionamento orizzontale deve essere relativo al margine interno della pagina corrente (il margine sinistro nelle pagine dispari, quello destro nelle pagine pari). |
| OutsideMargin | 7 | Specifica che il posizionamento orizzontale deve essere relativo al margine esterno della pagina corrente (il margine destro nelle pagine dispari, quello sinistro nelle pagine pari). |
| Default | n/a | Il valore predefinito è [Column](./). |


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


Mostra come inserire un'immagine flottante al centro di una pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un'immagine flottante che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
