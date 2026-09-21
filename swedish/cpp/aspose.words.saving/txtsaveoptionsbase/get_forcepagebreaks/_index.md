---
title: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks metod"
linktitle: "get_ForcePageBreaks"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks metod. Tillåter att ange om sidbrytningar ska bevaras vid export. Standardvärdet är false i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.saving/txtsaveoptionsbase/get_forcepagebreaks/
---
## TxtSaveOptionsBase::get_ForcePageBreaks method


Tillåter att ange om sidbrytningar ska bevaras under export. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks() const
```


## Exempel



Visar hur man anger om sidbrytningar ska bevaras när ett dokument exporteras till ren text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3");

// Skapa ett "TxtSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"
// metod för att ändra hur vi sparar dokumentet som klartext.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Aspose.Words "Document"-objekten har sidbrytningar, precis som Microsoft Word-dokument.
// Sparaformat som ".txt" är en kontinuerlig textmassa utan sidbrytningar.
// Ställ in egenskapen "ForcePageBreaks" till "true" för att bevara alla sidbrytningar i form av '\\f'-tecken.
// Ställ in egenskapen "ForcePageBreaks" till "false" för att ta bort alla sidbrytningar.
saveOptions->set_ForcePageBreaks(forcePageBreaks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt", saveOptions);

// Om vi laddar ett klartextdokument med sidbrytningar,
// kommer "Document"-objektet att använda dem för att dela upp kroppen i sidor.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"TxtSaveOptions.PageBreaks.txt");

ASSERT_EQ(forcePageBreaks ? 3 : 1, doc->get_PageCount());
```

## Se även

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
