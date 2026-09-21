---
title: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions metod"
linktitle: "get_OutlineOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions metod. Tillåter att ange konturalternativ i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


Tillåter att ange konturalternativ.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## Anmärkningar


Observera att alternativet [ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) inte kommer att fungera när du sparar till XPS.

## Exempel



Visar hur man begränsar rubriknivån som kommer att visas i konturen av ett sparat XPS-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga rubriker som kan fungera som innehållsförteckningsposter på nivå 1, 2 och sedan 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Det resulterande XPS-dokumentet kommer att innehålla en kontur, en innehållsförteckning som listar rubriker i dokumentets huvuddel.
// Att klicka på en post i denna kontur tar oss till platsen för dess respektive rubrik.
// Ställ in egenskapen "HeadingsOutlineLevels" till "2" för att utesluta alla rubriker vars nivåer är över 2 från konturen.
// De två sista rubrikerna vi har infogat ovan kommer inte att visas.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Se även

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
