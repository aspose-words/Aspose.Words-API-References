---
title: Aspose::Words::DocumentBase::ImportNode method
linktitle: ImportNode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBase::ImportNode method. Imports a node from another document to the current document in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Imports a node from another document to the current document.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | The node being imported. |
| isImportChildren | bool | **true** to import all child nodes recursively; otherwise, **false**. |

### ReturnValue

The cloned node that belongs to the current document.
## Remarks


This method uses the [UseDestinationStyles](../../importformatmode/) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [InsertBefore1()</see> or <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

## Examples



Shows how to import a node from one document to another. 
```cpp
auto srcDoc = MakeObject<Document>();
auto dstDoc = MakeObject<Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(dstDoc, u"Destination document first paragraph text."));

// Every node has a parent document, which is the document that contains the node.
// Inserting a node into a document that the node does not belong to will throw an exception.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(dstDoc->AppendChild(srcDoc->get_FirstSection()), System::ArgumentException);

// Use the ImportNode method to create a copy of a node, which will have the document
// that called the ImportNode method set as its new owner document.
auto importedSection = System::ExplicitCast<Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// We can now insert the node into the document.
dstDoc->AppendChild(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(SaveFormat::Text));
```

## See Also

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Imports a node from another document to the current document with an option to control formatting.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to imported. |
| isImportChildren | bool | **true** to import all child nodes recursively; otherwise, **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |

### ReturnValue

The cloned, imported node. The node belongs to the destination document, but has no parent.
## Remarks


This overload is useful to control how styles and list formatting are imported.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [InsertBefore1()</see> or <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

## Examples



Shows how to import node from source document to destination document with specific options. 
```cpp
// Create two documents and add a character style to each document.
// Configure the styles to have the same name, but different text formatting.
auto srcDoc = MakeObject<Document>();
SharedPtr<Style> srcStyle = srcDoc->get_Styles()->Add(StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = MakeObject<DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = MakeObject<Document>();
SharedPtr<Style> dstStyle = dstDoc->get_Styles()->Add(StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = MakeObject<DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Import the Section from the destination document into the source document, causing a style name collision.
// If we use destination styles, then the imported source text with the same style name
// as destination text will adopt the destination style.
auto importedSection = System::ExplicitCast<Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// If we use ImportFormatMode.KeepDifferentStyles, the source style is preserved,
// and the naming clash resolves by adding a suffix.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## See Also

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
