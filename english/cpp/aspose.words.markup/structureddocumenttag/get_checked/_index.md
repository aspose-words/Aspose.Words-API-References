---
title: Aspose::Words::Markup::StructuredDocumentTag::get_Checked method
linktitle: get_Checked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_Checked method. Gets/Sets current state of the Checkbox SDT. Default value for this property is false in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Remarks


Accessing this property will only work for [Checkbox](../../sdttype/) SDT types.

For all other SDT types exception will occur.

## Examples



Show how to create a structured document tag in the form of a check box. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
