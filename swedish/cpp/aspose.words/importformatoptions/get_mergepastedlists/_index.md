---
title: "Aspose::Words::ImportFormatOptions::get_MergePastedLists metod"
linktitle: "get_MergePastedLists"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_MergePastedLists metod. Hämtar eller anger ett booleskt värde som specificerar om inklistrade listor ska slås ihop med omgivande listor. Standardvärdet är false i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Hämtar eller anger ett booleskt värde som specificerar om inklistrade listor ska slås ihop med omgivande listor. Standardvärdet är **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Exempel



Visar hur man slår ihop listor från ett dokument.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Ställ in egenskapen "MergePastedLists" till "true" så att inklistrade listor slås ihop med omgivande listor.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
