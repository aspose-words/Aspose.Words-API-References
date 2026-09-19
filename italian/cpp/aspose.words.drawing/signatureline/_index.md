---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::SignatureLine class. Fornisce l'accesso alle proprietà della linea di firma. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Fornisce l'accesso alle proprietà della linea di firma. Per saperne di più, visita l'articolo di documentazione [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLine : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Ottiene o imposta un valore che indica se il firmatario può aggiungere commenti nella finestra di dialogo di firma. Il valore predefinito per questa proprietà è **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Ottiene o imposta un valore che indica se le istruzioni predefinite sono visualizzate nella finestra di dialogo Firma. Il valore predefinito per questa proprietà è **true**. |
| [get_Email](./get_email/)() | Ottiene o imposta l'indirizzo e‑mail del firmatario suggerito. Il valore predefinito per questa proprietà è **empty string**. |
| [get_Id](./get_id/)() | Ottiene o imposta l'identificatore per questa linea di firma. Questo identificatore può essere associato a una firma digitale, quando si firma il documento utilizzando [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). Questo valore deve essere univoco e, per impostazione predefinita, viene generato casualmente un nuovo Guid (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | Ottiene o imposta le istruzioni per il firmatario visualizzate durante la firma della linea di firma. Questa proprietà viene ignorata se [DefaultInstructions](./get_defaultinstructions/) è impostata. Il valore predefinito per questa proprietà è **stringa vuota**. |
| [get_IsSigned](./get_issigned/)() | Indica che la linea di firma è firmata con una firma digitale. |
| [get_IsValid](./get_isvalid/)() | Indica che la linea di firma è firmata con una firma digitale e che questa firma digitale è valida. |
| [get_ProviderId](./get_providerid/)() | Ottiene o imposta l'identificatore del provider di firma per questa linea di firma. Il valore predefinito è "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Ottiene o imposta un valore che indica se la data di firma è visualizzata nella riga della firma. Il valore predefinito per questa proprietà è **true**. |
| [get_Signer](./get_signer/)() | Ottiene o imposta il firmatario suggerito per la linea di firma. Il valore predefinito per questa proprietà è **stringa vuota**. |
| [get_SignerTitle](./get_signertitle/)() | Ottiene o imposta il titolo del firmatario suggerito (ad esempio, Manager). Il valore predefinito per questa proprietà è **stringa vuota**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Metodo set per [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
