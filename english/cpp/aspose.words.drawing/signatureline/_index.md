---
title: SignatureLine
second_title: Aspose.Words for C++ API Reference
description: Provides access to signature line properties. To learn more, visit the  documentation article.
type: docs
weight: 157
url: /cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


Provides access to signature line properties. To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class SignatureLine : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is **true**. |
| [get_Email](./get_email/)() | Gets or sets suggested signer's e-mail address. Default value for this property is **empty string**. |
| [get_Id](./get_id/)() | Gets or sets identifier for this signature line. This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). This value must be unique and by default it is randomly generated new Guid (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | Gets or sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [DefaultInstructions](./get_defaultinstructions/) is set. Default value for this property is **empty string**. |
| [get_IsSigned](./get_issigned/)() | Indicates that signature line is signed by digital signature. |
| [get_IsValid](./get_isvalid/)() | Indicates that signature line is signed by digital signature and this digital signature is valid. |
| [get_ProviderId](./get_providerid/)() | Gets or sets signature provider identifier for this signature line. Default value is "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is **true**. |
| [get_Signer](./get_signer/)() | Gets or sets suggested signer of the signature line. Default value for this property is **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | Gets or sets suggested signer's title (for example, Manager). Default value for this property is **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Setter for [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Setter for [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Setter for [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | Setter for [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Setter for [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Setter for [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | Setter for [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Setter for [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Setter for [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

## Examples



Shows how to create a line for a signature and insert it into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto options = MakeObject<SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// Insert a shape that will contain a signature line, whose appearance we will
// customize using the "SignatureLineOptions" object we have created above.
// If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
// we will need to supply negative x and y coordinates to bring the shape into view.
SharedPtr<Shape> shape = builder->InsertSignatureLine(options, RelativeHorizontalPosition::RightMargin, -170.0, RelativeVerticalPosition::BottomMargin,
                                                      -60.0, WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Verify the properties of our signature line via its Shape object.
SharedPtr<SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(ArtifactsDir + u"Shape.SignatureLine.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)
