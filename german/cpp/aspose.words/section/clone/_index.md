---
title: "Aspose::Words::Section::Clone Methode"
linktitle: "Klonen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::Clone Methode. Erstellt ein Duplikat dieses Abschnitts in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/section/clone/
---
## Section::Clone method


Erstellt ein Duplikat dieses Abschnitts.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## Beispiele



Zeigt, wie man Abschnitte in einem Dokument hinzufügt und entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Löschen Sie den ersten Abschnitt aus dem Dokument.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Fügen Sie eine Kopie des jetzt ersten Abschnitts am Ende des Dokuments an.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## Siehe auch

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
