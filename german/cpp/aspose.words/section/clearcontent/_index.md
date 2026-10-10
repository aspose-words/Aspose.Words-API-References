---
title: "Aspose::Words::Section::ClearContent Methode"
linktitle: "ClearContent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Section::ClearContent Methode. Löscht den Abschnitt in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Löscht den Abschnitt.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Hinweise


Der Text von [Body](../get_body/) wird gelöscht, es bleibt nur ein leerer Absatz übrig, der den Abschnittsumbruch darstellt.

Der Text aller Kopf- und Fußzeilen wird gelöscht, aber die [HeaderFooter](../../headerfooter/)-Objekte selbst werden nicht entfernt.

## Beispiele



Zeigt, wie man den Inhalt eines Abschnitts löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Das Ausführen der Methode "ClearContent" entfernt den gesamten Inhalt des Abschnitts
// lässt jedoch einen leeren Absatz zurück, um erneut Inhalt hinzuzufügen.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## Siehe auch

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
