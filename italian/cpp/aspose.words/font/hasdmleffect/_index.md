---
title: "Metodo Aspose::Words::Font::HasDmlEffect"
linktitle: "HasDmlEffect"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::HasDmlEffect. Verifica se un particolare effetto di testo DrawingML è applicato in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


Verifica se è applicato un determinato effetto di testo DrawingML.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | Tipo di effetto di testo DrawingML. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

## Esempi



Mostra come verificare se una sequenza visualizza un effetto di testo DrawingML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## Vedi anche

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
