---
title: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection metod"
linktitle: "get_DocumentDirection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection metod. Hämtar eller anger en dokumentriktning. Standardvärdet är LeftToRight i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


Hämtar eller anger en dokumentriktning. Standardvärdet är [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


## Exempel



Visar hur man upptäcker textens riktning i ett klartextdokument.
```cpp
// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Ställ in egenskapen "DocumentDirection" till "DocumentDirection.Auto" för att automatiskt upptäcka
// riktningen för varje textparagraf som Aspose.Words laddar från klartext.
// Varje stycke's "Bidi"-egenskap lagrar dess riktning.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Detektera hebreisk text som från höger till vänster.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Detektera engelsk text som från höger till vänster.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Se även

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
