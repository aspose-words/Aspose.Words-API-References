---
title: Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior method
linktitle: get_SmartStyleBehavior
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior method. Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is false in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Gets or sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Remarks


When this option is **enabled**, the source style will be expanded into a direct attributes inside a destination document, if [KeepSourceFormatting](../../importformatmode/) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing destination attributes will not be overridden, including lists.

## Examples



Shows how to resolve duplicate styles while inserting documents. 
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
// If we insert the clone into the original document, the two styles with the same name will cause a clash.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
// Aspose.Words will resolve style clashes by converting source document styles.
// with the same names as destination styles into direct paragraph attributes.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## See Also

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
