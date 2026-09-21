---
title: "Aspose::Words::BaselineAlignment enum"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::BaselineAlignment enum. Anger teckensnittens vertikala position på en rad i C++."
type: docs
weight: 80500
url: /sv/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Anger teckensnittets vertikala position på en rad.

```cpp
enum class BaselineAlignment
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Top | 0 | Justeras längs toppen av varje teckensnitt. |
| Centrerad | 1 | Justerar mittpunkterna för varje teckensnitt. |
| Baseline | 2 | Justeras till paragrafens baslinje. |
| Bottom | 3 | Justeras till botten av varje teckensnitt. |
| Auto | 4 | Baslinjen justeras automatiskt. |


## Exempel



Visar hur man ställer in teckensnittens vertikala position på en rad.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
