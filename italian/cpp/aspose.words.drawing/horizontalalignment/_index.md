---
title: "Enum Aspose::Words::Drawing::HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Drawing::HorizontalAlignment. Specifica l'allineamento orizzontale di una forma flottante, di un riquadro di testo o di una tabella flottante in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Specifica l'allineamento orizzontale di una forma fluttuante, di un riquadro di testo o di una tabella fluttuante.

```cpp
enum class HorizontalAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | L'oggetto è posizionato esplicitamente, di solito usando la sua proprietà **Left**. |
| Default | n/a | Stesso di [None](./). |
| Sinistra | 1 | Specifica che l'oggetto deve essere allineato a sinistra rispetto alla base di allineamento orizzontale. |
| Centro | 2 | Specifica che l'oggetto deve essere centrato rispetto alla base di allineamento orizzontale. |
| Destra | 3 | Specifica che l'oggetto deve essere allineato a destra rispetto alla base di allineamento orizzontale. |
| Interno | 4 | Specifica che l'oggetto deve trovarsi all'interno della base di allineamento orizzontale. |
| Esterno | 5 | Specifica che l'oggetto deve trovarsi al di fuori della base di allineamento orizzontale. |


## Esempi



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
