---
title: "Aspose::Words::Document::UnlinkFields metod"
linktitle: "UnlinkFields"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UnlinkFields metod. Avkopplar fält i hela dokumentet i C++."
type: docs
weight: 94000
url: /sv/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


Kopplar bort fält i hela dokumentet.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## Anmärkningar


Ersätter alla fält i hela dokumentet med deras senaste resultat.

För att avkoppla fält i en specifik del av dokumentet, använd [UnlinkFields](../../range/unlinkfields/).

## Exempel



Visar hur man avkopplar alla fält i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
