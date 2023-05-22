---
title: Aspose::Words::DocumentBuilder::InsertDocument method
linktitle: InsertDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertDocument method. Inserts a document at the cursor position in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words/documentbuilder/insertdocument/
---
## DocumentBuilder::InsertDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) method


Inserts a document at the cursor position.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Source document for inserting. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |

### ReturnValue

First node of the inserted content.

## See Also

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertDocument(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Inserts a document at the cursor position.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocument(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Source document for inserting. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Allows to specify options that affect formatting of a result document. |

### ReturnValue

First node of the inserted content.

## Examples



Shows how to resolve duplicate styles while inserting documents. 
```cpp
auto dstDoc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(dstDoc);

SharedPtr<Style> myStyle = builder->get_Document()->get_Styles()->Add(StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
// If we insert the clone into the original document, the two styles with the same name will cause a clash.
SharedPtr<Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
// Aspose.Words will resolve style clashes by converting source document styles.
// with the same names as destination styles into direct paragraph attributes.
auto options = MakeObject<ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(ArtifactsDir + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## See Also

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
