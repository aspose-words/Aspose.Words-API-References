---
title: "Aspose::Words::Drawing::SignatureLine::get_SignerTitle metodo"
linktitle: "get_SignerTitle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::SignatureLine::get_SignerTitle metodo. Ottiene o imposta il titolo suggerito del firmatario (ad esempio, Manager). Il valore predefinito per questa proprietà è stringa vuota in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.drawing/signatureline/get_signertitle/
---
## SignatureLine::get_SignerTitle method


Ottiene o imposta il titolo del firmatario suggerito (ad esempio, Manager). Il valore predefinito per questa proprietà è **stringa vuota**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_SignerTitle()
```


## Esempi



Mostra come creare una linea per una firma e inserirla in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// Inserisci una forma che conterrà una linea di firma, la cui apparenza noi
// personalizzeremo usando l'oggetto "SignatureLineOptions" che abbiamo creato sopra.
// Se inseriamo una forma le cui coordinate originano dall'angolo in basso a destra della pagina,
// dovremo fornire coordinate x e y negative per portare la forma in vista.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Verifica le proprietà della nostra linea di firma tramite il suo oggetto Shape.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## Vedi anche

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
