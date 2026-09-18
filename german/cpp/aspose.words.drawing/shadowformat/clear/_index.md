---
title: "Aspose::Words::Drawing::ShadowFormat::Clear Methode"
linktitle: "Clear"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShadowFormat::Clear Methode. Löscht das Schattenformat in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Löscht die Schattenformatierung.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
```


## Beispiele



Zeigt, wie man mit einer Schattenformatierung für die Form arbeitet.
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

## Siehe auch

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
