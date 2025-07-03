---
title: Aspose::Words::Drawing::SignatureLine::get_Instructions method
linktitle: get_Instructions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::SignatureLine::get_Instructions method. Gets or sets instructions to the signer that are displayed on signing the signature line. This property is ignored if DefaultInstructions is set. Default value for this property is empty string in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/signatureline/get_instructions/
---
## SignatureLine::get_Instructions method


Gets or sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [DefaultInstructions](../get_defaultinstructions/) is set. Default value for this property is **empty string**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_Instructions()
```


## Examples



Shows how to create a line for a signature and insert it into a document. 
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

// Insert a shape that will contain a signature line, whose appearance we will
// customize using the "SignatureLineOptions" object we have created above.
// If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
// we will need to supply negative x and y coordinates to bring the shape into view.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// Verify the properties of our signature line via its Shape object.
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

## See Also

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
