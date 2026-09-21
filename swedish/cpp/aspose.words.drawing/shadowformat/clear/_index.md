---
title: "Aspose::Words::Drawing::ShadowFormat::Clear‑metod"
linktitle: "Clear"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShadowFormat::Clear method. Rensar skuggformat i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Rensar skuggformat.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
```


## Exempel



Visar hur man arbetar med skuggformatering för formen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## Se även

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
