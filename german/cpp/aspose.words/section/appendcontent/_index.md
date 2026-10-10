---
title: "Aspose::Words::Section::AppendContent Methode"
linktitle: "AppendContent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::AppendContent Methode. Fügt eine Kopie des Inhalts des Quellabschnitts am Ende dieses Abschnitts in C++ ein."
type: docs
weight: 4000
url: /de/cpp/aspose.words/section/appendcontent/
---
## Section::AppendContent method


Fügt eine Kopie des Inhalts des Quellabschnitts am Ende dieses Abschnitts ein.

```cpp
void Aspose::Words::Section::AppendContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | Der Abschnitt, von dem der Inhalt kopiert werden soll. |
## Hinweise


Nur der Inhalt von [Body](../get_body/) des Quellabschnitts wird kopiert, Seitenlayout, Kopf- und Fußzeilen werden nicht kopiert.

Die Knoten werden automatisch importiert, wenn der Quellabschnitt zu einem anderen Dokument gehört.

Im Ziel-Dokument wird kein neuer Abschnitt erstellt.

## Beispiele



Zeigt, wie man den Inhalt eines Abschnitts an einen anderen Abschnitt anhängt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// Fügen Sie den Inhalt des ersten Abschnitts am Anfang des dritten Abschnitts ein.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Fügen Sie den Inhalt des zweiten Abschnitts am Ende des dritten Abschnitts ein.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// Die Methoden "PrependContent" und "AppendContent" haben keine neuen Abschnitte erstellt.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## Siehe auch

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
