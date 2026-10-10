---
title: "Aspose::Words::Font::get_SmallCaps metod"
linktitle: "get_SmallCaps"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_SmallCaps metod. Sant om teckensnittet är formaterat som små versaler i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words/font/get_smallcaps/
---
## Font::get_SmallCaps method


Sant om teckensnittet är formaterat som små versaler.

```cpp
bool Aspose::Words::Font::get_SmallCaps()
```


## Exempel



Visar hur man formaterar en run för att visa dess innehåll med versaler.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Det finns två sätt att få en run att visa sin gemena text i versaler utan att ändra innehållet.
// 1 -  Ställ in AllCaps-flagg för att visa alla tecken i vanliga versaler:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  Ställ in SmallCaps-flagg för att visa alla tecken i små versaler:
// Om ett tecken är gemener visas det i sin versalform
// men har samma höjd som gemener (fontens x-höjd).
// Tecken som ursprungligen var versaler ser likadant ut.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
