---
title: StructuredDocumentTag
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of the Structured document tag class.
type: docs
weight: 14
url: /cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Initializes a new instance of the **Structured document tag** class.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| type | Aspose::Words::Markup::SdtType | Type of SDT node. |
| level | Aspose::Words::Markup::MarkupLevel | Level of SDT node within the document. |
## Remarks


The following types of SDT can be created:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



## Examples



Show how to create a structured document tag in the form of a check box. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto sdtCheckBox = MakeObject<StructuredDocumentTag>(doc, SdtType::Checkbox, MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.CheckBox.docx");
```

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
