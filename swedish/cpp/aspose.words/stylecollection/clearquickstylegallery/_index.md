---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery‑metod"
linktitle: "ClearQuickStyleGallery"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery‑metod. Tar bort alla stilar från Quick Style Gallery‑panelen i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Tar bort alla stilar från Quick [Style](../../style/)-galleripanelen.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Exempel



Visar hur man tar bort stilar från [Style](../../style/)-galleripanelen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Observera att borttagning av stilar för närvarande endast fungerar med DOCX-format.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## Se även

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
