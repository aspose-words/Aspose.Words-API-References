---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore Methode"
linktitle: "get_PageBreakBefore"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore Methode. True, wenn ein Seitenumbruch vor dem Absatz in C++ erzwungen wird."
type: docs
weight: 27000
url: /de/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


True, wenn ein Seitenumbruch vor dem Absatz erzwungen wird.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Beispiele



Zeigt, wie man Absätze mit Seitenumbrüchen am Anfang erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzen Sie dieses Flag auf "true", um einen Seitenumbruch am Anfang jedes Absatzes anzuwenden
// den der Dokument-Builder unter dieser ParagraphFormat-Konfiguration erstellt.
// Der erste Absatz erhält keinen Seitenumbruch.
// Lassen Sie dieses Flag auf "false", um jeden neuen Absatz auf derselben Seite zu beginnen
// wie der vorherige, vorausgesetzt, es ist genügend Platz vorhanden.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
