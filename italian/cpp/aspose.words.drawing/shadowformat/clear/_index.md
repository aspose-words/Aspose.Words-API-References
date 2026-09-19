---
title: "Metodo Aspose::Words::Drawing::ShadowFormat::Clear"
linktitle: "Cancella"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShadowFormat::Clear. Cancella il formato dell'ombra in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Cancella la formattazione dell'ombra.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
```


## Esempi



Mostra come lavorare con la formattazione dell'ombra per la forma.
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

## Vedi anche

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
