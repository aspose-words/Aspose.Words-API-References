---
title: "Aspose::Words::Font::get_NoProofing metod"
linktitle: "get_NoProofing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_NoProofing metod. Sant när de formaterade tecknen inte ska stavningskontrolleras i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


Sant när de formaterade tecknen inte ska rättas stavningsmässigt.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Exempel



Visar hur man förhindrar att text stavningskontrolleras av Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Vanligtvis markerar Microsoft Word stavfel med en hackig röd understrykning.
// Vi kan avaktivera "NoProofing"-flaggan för att skapa en del av texten som
// bypassar stavningskontrollen samtidigt som den helt inaktiveras.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
