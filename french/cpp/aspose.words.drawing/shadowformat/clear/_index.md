---
title: "Aspose::Words::Drawing::ShadowFormat::Clear méthode"
linktitle: "Clear"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShadowFormat::Clear méthode. Efface le format d'ombre en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat::Clear method


Efface le format d'ombre.

```cpp
void Aspose::Words::Drawing::ShadowFormat::Clear()
```


## Exemples



Montre comment travailler avec le format d'ombre pour la forme.
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

## Voir aussi

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
