---
title: get_Checked
second_title: Aspose.Words for C++ API Reference
description: Gets/Sets current state of the Checkbox SDT. Default value for this property is false.
type: docs
weight: 92
url: /cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag.get_Checked method


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is false.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```


Accessing this property will only work for **Checkbox** SDT types.

For all other SDT types exception will occur.

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

