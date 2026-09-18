---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery Methode"
linktitle: "ClearQuickStyleGallery"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery Methode. Entfernt alle Stile aus dem Quick‑Style‑Gallery‑Panel in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Entfernt alle Stile aus dem Quick‑[Style](../../style/)-Gallery‑Panel.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Beispiele



Zeigt, wie Stile aus dem [Style](../../style/)-Gallery‑Panel entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Beachten Sie, dass das Entfernen von Stilen derzeit nur im DOCX‑Format funktioniert.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## Siehe auch

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
