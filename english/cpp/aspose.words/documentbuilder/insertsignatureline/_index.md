---
title: Aspose::Words::DocumentBuilder::InsertSignatureLine method
linktitle: InsertSignatureLine
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertSignatureLine method. Inserts a signature line at the current position in C++.'
type: docs
weight: 46000
url: /cpp/aspose.words/documentbuilder/insertsignatureline/
---
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&) method


Inserts a signature line at the current position.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | The object that stores parameters of creating signature line. |

### ReturnValue

The signature line node that was just inserted.

## Examples



Shows how to sign a document with a personal certificate and a signature line. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto signatureLineOptions = MakeObject<SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

SharedPtr<SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = MakeObject<SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

SharedPtr<CertificateHolder> certHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");

DigitalSignatureUtil::Sign(ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.docx",
                           ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = MakeObject<Document>(ArtifactsDir + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertSignatureLine(const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, Aspose::Words::Drawing::WrapType) method


Inserts a signature line at the specified position.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertSignatureLine(const System::SharedPtr<Aspose::Words::SignatureLineOptions> &signatureLineOptions, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, Aspose::Words::Drawing::WrapType wrapType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| signatureLineOptions | const System::SharedPtr\<Aspose::Words::SignatureLineOptions\>\& | The object that stores parameters of creating signature line. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Specifies where the distance to the signature line is measured from. |
| left | double | Distance in points from the origin to the left side of the signature line. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Specifies where the distance to the signature line measured from. |
| top | double | Distance in points from the origin to the top side of the signature line. |
| wrapType | Aspose::Words::Drawing::WrapType | Specifies how to wrap text around the signature line. |

### ReturnValue

The signature line node that was just inserted.
## Remarks


You can change the image size, location, positioning method and other settings using the [Shape](../../../aspose.words.drawing/shape/) object returned by this method.

## Examples



Shows how to insert an inline signature line into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto options = MakeObject<SignatureLineOptions>();
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Manager");
options->set_Email(u"johndoe@aspose.com");
options->set_ShowDate(true);
options->set_DefaultInstructions(false);
options->set_Instructions(u"Please sign here.");
options->set_AllowComments(true);

builder->InsertSignatureLine(options, RelativeHorizontalPosition::RightMargin, 2.0, RelativeVerticalPosition::Page, 3.0, WrapType::Inline);

// The signature line can be signed in Microsoft Word by double clicking it.
doc->Save(ArtifactsDir + u"DocumentBuilder.SignatureLineInline.docx");
```

## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [SignatureLineOptions](../../signaturelineoptions/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
