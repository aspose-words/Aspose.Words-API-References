---
title: "Metodo Aspose::Words::Font::get_Position"
linktitle: "get_Position"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Position. Ottiene o imposta la posizione del testo (in punti) rispetto alla linea di base. Un numero positivo solleva il testo, e un numero negativo lo abbassa in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


Ottiene o imposta la posizione del testo (in punti) rispetto alla linea di base. Un numero positivo solleva il testo, e un numero negativo lo abbassa.

```cpp
double Aspose::Words::Font::get_Position()
```


## Esempi



Mostra come formattare il testo per spostare la sua posizione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Solleva questo segmento di testo di 5 punti sopra la linea di base.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Abbassa questo segmento di testo di 10 punti sotto la linea di base.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Aggiungi un segmento di testo normale.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Aggiungi un segmento di testo che appare come pedice.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Aggiungi un segmento di testo che appare come apice.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
