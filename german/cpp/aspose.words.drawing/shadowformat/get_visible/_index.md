---
title: "Aspose::Words::Drawing::ShadowFormat::get_Visible Methode"
linktitle: "get_Visible"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShadowFormat::get_Visible Methode. Gibt true zurück, wenn die auf diese Instanz angewendete Formatierung in C++ sichtbar ist."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/shadowformat/get_visible/
---
## ShadowFormat::get_Visible method


Gibt **true** zurück, wenn die auf diese Instanz angewendete Formatierung sichtbar ist.

```cpp
bool Aspose::Words::Drawing::ShadowFormat::get_Visible()
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
