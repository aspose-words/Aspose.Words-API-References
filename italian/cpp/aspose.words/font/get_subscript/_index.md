---
title: "Metodo Aspose::Words::Font::get_Subscript"
linktitle: "get_Subscript"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Subscript. Vero se il carattere è formattato come pedice in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words/font/get_subscript/
---
## Font::get_Subscript method


True se il font è formattato come pedice.

```cpp
bool Aspose::Words::Font::get_Subscript()
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
