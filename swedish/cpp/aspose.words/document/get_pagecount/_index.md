---
title: "Aspose::Words::Document::get_PageCount‑metod"
linktitle: "get_PageCount"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_PageCount‑metod. Hämtar antalet sidor i dokumentet enligt den senaste sidlayoutoperationen i C++."
type: docs
weight: 43000
url: /sv/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Hämtar antalet sidor i dokumentet enligt den senaste sidlayoutoperationen.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Exempel



Visar hur man räknar antalet sidor i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Verifiera det förväntade sidantalet i dokumentet.
ASSERT_EQ(3, doc->get_PageCount());

// Att hämta PageCount‑egenskapen utlöste dokumentets sidlayout för att beräkna värdet.
// Denna operation behöver inte upprepas när dokumentet renderas till ett fast sidformat för sparande,
// såsom .pdf. Så kan du spara tid, särskilt med mer komplexa dokument.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
