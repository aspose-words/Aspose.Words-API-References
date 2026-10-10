---
title: "Aspose::Words::ParagraphFormat::get_BaselineAlignment method"
linktitle: "get_BaselineAlignment"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_BaselineAlignment method. Hämtar eller anger typsnittets vertikala position på en rad i C++."
type: docs
weight: 5500
url: /sv/cpp/aspose.words/paragraphformat/get_baselinealignment/
---
## ParagraphFormat::get_BaselineAlignment method


Hämtar eller anger teckensnittets vertikala position på en rad.

```cpp
Aspose::Words::BaselineAlignment Aspose::Words::ParagraphFormat::get_BaselineAlignment()
```


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

* Enum [BaselineAlignment](../../baselinealignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
