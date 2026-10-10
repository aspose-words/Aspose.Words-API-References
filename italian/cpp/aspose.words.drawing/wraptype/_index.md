---
title: "Aspose::Words::Drawing::WrapType enum"
linktitle: "WrapType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::WrapType enum. Specifica come il testo viene avvolto attorno a una forma o immagine in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Specifica come il testo è avvolto attorno a una forma o immagine.

```cpp
enum class WrapType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 3 | Nessun avvolgimento del testo attorno alla forma. La forma è posizionata dietro o davanti al testo. |
| Inline | 0 | La forma rimane sullo stesso livello del testo ed è trattata come un carattere. |
| TopBottom | 1 | Il testo si ferma in cima alla forma e riprende sulla riga sotto la forma. |
| Square | 2 | Avvolge il testo attorno a tutti i lati del riquadro quadrato della forma. |
| Tight | 4 | Avvolge strettamente i bordi della forma, invece di avvolgere il riquadro. |
| Through | 5 | Come Tight, ma avvolge all'interno di qualsiasi parte della forma che sia aperta. |


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
