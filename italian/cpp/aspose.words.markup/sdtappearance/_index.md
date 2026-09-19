---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::SdtAppearance enum. Specifica l'aspetto di un tag di documento strutturato in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


Specifica l'aspetto di un tag di documento strutturato.

```cpp
enum class SdtAppearance
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| BoundingBox | 0 | Rappresenta un tag di documento strutturato mostrato come un rettangolo ombreggiato o una bounding box. |
| Tags | 1 | Rappresenta un tag di documento strutturato mostrato come marcatori di inizio e fine. |
| Nascosto | 2 | Rappresenta un tag di documento strutturato che non è mostrato. |
| Default | n/a | Il valore predefinito è [BoundingBox](./). |


## Esempi



Mostra come visualizzare il tag attorno al contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
