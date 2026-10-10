---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::LayoutFlow enum. Determina il flusso del layout del testo in una casella di testo in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Determina il flusso del layout del testo in una casella di testo.

```cpp
enum class LayoutFlow
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Orizzontale | 0 | Il testo viene visualizzato orizzontalmente. |
| TopToBottomIdeographic | 1 | Il testo ideografico viene visualizzato verticalmente. |
| BottomToTop | 2 | Il testo viene visualizzato verticalmente. |
| TopToBottom | 3 | Il testo viene visualizzato verticalmente. |
| HorizontalIdeographic | 4 | Il testo ideografico viene visualizzato orizzontalmente. |
| Verticale | 5 | Il testo viene visualizzato verticalmente. |


## Esempi



Mostra come aggiungere testo a una casella di testo e modificarne l'orientamento
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
