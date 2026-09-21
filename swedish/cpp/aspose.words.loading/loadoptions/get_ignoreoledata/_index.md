---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData metod"
linktitle: "get_IgnoreOleData"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData metod. Anger om OLE-data ska ignoreras i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


Anger om OLE-data ska ignoreras.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Anmärkningar


Att ignorera OLE-data kan minska minnesanvändningen och öka prestandan utan dataförlust i fall då målformatet inte stöder OLE-objekt.

Standardvärdet är **false**.

## Exempel



Visar hur man ignorerar OLE-data vid laddning.
```cpp
// Att ignorera OLE-data kan minska minnesförbrukningen och öka prestandan
// utan dataförlust i ett fall då målformatet inte stöder OLE-objekt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
