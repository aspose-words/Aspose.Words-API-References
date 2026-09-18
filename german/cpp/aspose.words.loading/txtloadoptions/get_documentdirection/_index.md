---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection Methode"
linktitle: "get_DocumentDirection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection Methode. Gibt die Dokumentenrichtung zurück oder legt sie fest. Der Standardwert ist LeftToRight in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


Gibt die Dokumentenrichtung zurück oder legt sie fest. Der Standardwert ist [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


## Beispiele



Zeigt, wie man die Textflussrichtung eines Klartextdokuments erkennt.
```cpp
// Erstelle ein \"TxtLoadOptions\"‑Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Setze die Eigenschaft \"DocumentDirection\" auf \"DocumentDirection.Auto\", erkennt automatisch
// die Richtung jedes Textabsatzes, den Aspose.Words aus Klartext lädt.
// Die \"Bidi\"‑Eigenschaft jedes Absatzes speichert dessen Richtung.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Hebräischen Text als rechts‑nach‑links erkennen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Englischen Text als rechts‑nach‑links erkennen.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Siehe auch

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
