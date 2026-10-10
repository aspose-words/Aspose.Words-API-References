---
title: "Aspose::Words::Fonts::FontInfoCollection::Contains Methode"
linktitle: "Contains"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfoCollection::Contains Methode. Bestimmt, ob die Sammlung eine Schrift mit dem angegebenen Namen in C++ enthält."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


Bestimmt, ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Groß-/Kleinschreibung ignorierender Name der zu findenden Schrift. |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

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
