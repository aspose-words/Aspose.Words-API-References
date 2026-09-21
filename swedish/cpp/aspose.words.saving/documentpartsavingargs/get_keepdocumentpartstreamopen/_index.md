---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen‑metoden"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen‑metoden. Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att ha sparat en dokumentdel i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en dokumentdel har sparats.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Anmärkningar


Standard är **false** och Aspose.Words kommer att stänga den ström du angav i egenskapen [DocumentPartStream](../get_documentpartstream/) efter att ha skrivit en dokumentdel till den. Ange **true** för att hålla strömmen öppen. Observera att huvudutdata‑strömmen som tillhandahålls i anropet till [Save()](../) eller [Save()](../) aldrig kommer att stängas av Aspose.Words även om [KeepDocumentPartStreamOpen](./) är satt till **false**.

## Se även

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
