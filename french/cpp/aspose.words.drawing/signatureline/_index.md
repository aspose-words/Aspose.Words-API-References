---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::SignatureLine class. Fournit l'accès aux propriétés de la ligne de signature. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Fournit l'accès aux propriétés de la ligne de signature. Pour en savoir plus, consultez l'article de documentation [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) .

```cpp
class SignatureLine : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Obtient ou définit une valeur indiquant que le signataire peut ajouter des commentaires dans la boîte de dialogue Sign. La valeur par défaut de cette propriété est **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Obtient ou définit une valeur indiquant que les instructions par défaut sont affichées dans la boîte de dialogue Sign. La valeur par défaut de cette propriété est **true**. |
| [get_Email](./get_email/)() | Obtient ou définit l'adresse e‑mail du signataire suggéré. La valeur par défaut de cette propriété est **empty string**. |
| [get_Id](./get_id/)() | Obtient ou définit l'identifiant de cette ligne de signature. Cet identifiant peut être associé à une signature numérique, lors de la signature du document à l'aide de [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). Cette valeur doit être unique et, par défaut, elle est générée aléatoirement comme nouveau Guid (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | Obtient ou définit les instructions destinées au signataire qui sont affichées lors de la signature de la ligne de signature. Cette propriété est ignorée si [DefaultInstructions](./get_defaultinstructions/) est définie. La valeur par défaut de cette propriété est **empty string**. |
| [get_IsSigned](./get_issigned/)() | Indique que la ligne de signature est signée par une signature numérique. |
| [get_IsValid](./get_isvalid/)() | Indique que la ligne de signature est signée par une signature numérique et que cette signature numérique est valide. |
| [get_ProviderId](./get_providerid/)() | Obtient ou définit l'identifiant du fournisseur de signature pour cette ligne de signature. La valeur par défaut est "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Obtient ou définit une valeur indiquant que la date de signature est affichée dans la ligne de signature. La valeur par défaut de cette propriété est **true**. |
| [get_Signer](./get_signer/)() | Obtient ou définit le signataire suggéré de la ligne de signature. La valeur par défaut de cette propriété est **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Obtient ou définit le titre du signataire suggéré (par exemple, Manager). La valeur par défaut de cette propriété est **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment créer une ligne de signature et l'insérer dans un document.
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

// Insérez une forme qui contiendra une ligne de signature, dont l'apparence nous allons
// personnaliser en utilisant l'objet "SignatureLineOptions" que nous avons créé ci‑dessus.
// Si nous insérons une forme dont les coordonnées proviennent du coin inférieur droit de la page,
// nous devrons fournir des coordonnées x et y négatives pour faire apparaître la forme.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Vérifiez les propriétés de notre ligne de signature via son objet Shape.
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

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
