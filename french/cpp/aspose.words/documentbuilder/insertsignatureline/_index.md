---
title: "Aspose::Words::DocumentBuilder::InsertSignatureLine méthode"
linktitle: "InsertSignatureLine"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertSignatureLine méthode. Insère une ligne de signature à la position actuelle en C++."
type: docs
weight: 46000
url: /fr/cpp/aspose.words/documentbuilder/insertsignatureline/
---
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) method


Insère une ligne de signature à la position actuelle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | L'objet qui stocke les paramètres de création de la ligne de signature. |

### ReturnValue

Le nœud de ligne de signature qui vient d'être inséré.

## Exemples



Montre comment signer un document avec un certificat personnel et une ligne de signature.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto signatureLineOptions = System::MakeObject<Aspose::Words::SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx", get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Rouvrez notre document enregistré et vérifiez que les propriétés "IsSigned" et "IsValid" sont toutes deux égales à "true",
// indiquant que la ligne de signature contient une signature.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) method


Insère une ligne de signature à la position spécifiée.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, Aspose::Words::Drawing::WrapType wrapType)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | L'objet qui stocke les paramètres de création de la ligne de signature. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Spécifie à partir de quel point la distance à la ligne de signature est mesurée. |
| left | double | Distance en points de l'origine au côté gauche de la ligne de signature. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Spécifie à partir de quel point la distance à la ligne de signature est mesurée. |
| top | double | Distance en points de l'origine au côté supérieur de la ligne de signature. |
| wrapType | Aspose::Words::Drawing::WrapType | Spécifie comment envelopper le texte autour de la ligne de signature. |

### ReturnValue

Le nœud de ligne de signature qui vient d'être inséré.
## Remarques


Vous pouvez modifier la taille, l’emplacement, la méthode de positionnement et d’autres paramètres de l’image en utilisant l’objet [Shape](../../../aspose.words.drawing/shape/) retourné par cette méthode.

## Exemples



Montre comment insérer une ligne de signature en ligne dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Manager");
options->set_Email(u"johndoe@aspose.com");
options->set_ShowDate(true);
options->set_DefaultInstructions(false);
options->set_Instructions(u"Please sign here.");
options->set_AllowComments(true);

builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, 2.0, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 3.0, Aspose::Words::Drawing::WrapType::Inline);

// La ligne de signature peut être signée dans Microsoft Word en double-cliquant dessus.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineInline.docx");
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
