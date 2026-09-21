---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents metod"
linktitle: "get_MirrorIndents"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_MirrorIndents metod. Hämtar eller anger en flagga som indikerar huruvida vänster- och högermarginalerna har samma bredd i C++."
type: docs
weight: 24500
url: /sv/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Hämtar eller anger en flagga som indikerar om vänster- och högra indragen har samma bredd.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Exempel



Visa hur man gör vänster- och högermarginalerna lika.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
