---
title: "Aspose::Words::TextDmlEffect enum"
linktitle: "TextDmlEffect"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextDmlEffect enum. Effetto di testo Dml per le sequenze di testo in C++."
type: docs
weight: 122000
url: /it/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


Effetto di testo Dml per le run di testo.

```cpp
enum class TextDmlEffect
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Bagliore | 0 | Effetto bagliore, in cui un contorno sfocato colorato viene aggiunto al di fuori dei bordi dell'oggetto. |
| Riempimento | 1 | Effetto di sovrapposizione di riempimento. |
| Ombra | 2 | Effetto ombra. |
| Contorno | 3 | Effetto contorno. |
| Effect3D | 4 | Effetto 3D. |
| Riflesso | 5 | Effetto riflesso. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
