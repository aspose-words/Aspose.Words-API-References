---
title: "Aspose::Words::Fonts::FontInfoCollection::get_Count Methode"
linktitle: "get_Count"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfoCollection::get_Count Methode. Gibt die Anzahl der im Sammelobjekt enthaltenen Elemente in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück.

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## Beispiele



Zeigt Informationen über die Schriftarten, die im leeren Dokument vorhanden sind.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält 3 Standardschriftarten. Jede Schriftart im Dokument
// hat ein entsprechendes FontInfo-Objekt, das Details zu dieser Schriftart enthält.
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## Siehe auch

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
