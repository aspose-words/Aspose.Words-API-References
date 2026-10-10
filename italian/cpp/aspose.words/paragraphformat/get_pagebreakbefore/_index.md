---
title: "Metodo Aspose::Words::ParagraphFormat::get_PageBreakBefore"
linktitle: "get_PageBreakBefore"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_PageBreakBefore. True se un'interruzione di pagina è forzata prima del paragrafo in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


Vero se viene forzata un'interruzione di pagina prima del paragrafo.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Esempi



Mostra come creare paragrafi con interruzioni di pagina all'inizio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta questo flag su "true" per applicare un'interruzione di pagina all'inizio di ogni paragrafo
// che il document builder creerà con questa configurazione di ParagraphFormat.
// Il primo paragrafo non riceverà un'interruzione di pagina.
// Lascia questo flag su "false" per iniziare ogni nuovo paragrafo nella stessa pagina
// come il precedente, a condizione che ci sia spazio sufficiente.
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

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
