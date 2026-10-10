---
title: "Aspose::Words::HeaderFooter::get_IsLinkedToPrevious Methode"
linktitle: "get_IsLinkedToPrevious"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooter::get_IsLinkedToPrevious Methode. Wahr, wenn diese Kopf- oder Fußzeile in C++ mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt verknüpft ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words/headerfooter/get_islinkedtoprevious/
---
## HeaderFooter::get_IsLinkedToPrevious method


True, wenn diese Kopf‑ oder Fußzeile mit der entsprechenden Kopf‑ bzw. Fußzeile im vorherigen Abschnitt verknüpft ist.

```cpp
bool Aspose::Words::HeaderFooter::get_IsLinkedToPrevious()
```

## Hinweise


Standard ist **true**.

Hinweis: Wenn Sie eine Kopf- oder Fußzeile verlinken, wird ihr Inhalt gelöscht.

## Beispiele



Zeigt, wie Kopf- und Fußzeilen zwischen Abschnitten verknüpft werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Wechseln Sie zum ersten Abschnitt und erstellen Sie eine Kopfzeile und eine Fußzeile. Standardmäßig,
// werden die Kopf- und Fußzeile nur auf Seiten des Abschnitts angezeigt, der sie enthält.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Wir können die Kopf-/Fußzeilen eines Abschnitts mit den Kopf-/Fußzeilen des vorherigen Abschnitts verknüpfen
// um dem verknüpfenden Abschnitt zu ermöglichen, die Kopf-/Fußzeilen des verknüpften Abschnitts anzuzeigen.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Jeder Abschnitt behält weiterhin seine eigenen Kopf-/Fußzeilenobjekte. Wenn wir Abschnitte verknüpfen,
// zeigt der verknüpfende Abschnitt die Kopf-/Fußzeilen des verknüpften Abschnitts an, während er seine eigenen beibehält.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Verknüpfen Sie die Kopf-/Fußzeilen des dritten Abschnitts mit den Kopf-/Fußzeilen des zweiten Abschnitts.
// Der zweite Abschnitt ist bereits mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft,
// so erzeugt das Verknüpfen mit dem zweiten Abschnitt eine Verkettung.
// Der erste, zweite und nun der dritte Abschnitt werden alle die Kopfzeilen des ersten Abschnitts anzeigen.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// Wir können die Kopf-/Fußzeilen eines vorherigen Abschnitts trennen, indem wir beim Aufruf der Methode LinkToPrevious "false" übergeben.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Wir können mit dieser Methode auch nur einen bestimmten Typ von Kopf-/Fußzeile zum Verknüpfen auswählen.
// Der dritte Abschnitt hat jetzt dieselbe Fußzeile wie der zweite und erste Abschnitt, jedoch nicht die Kopfzeile.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Die Kopf-/Fußzeilen des ersten Abschnitts können sich nicht mit etwas verknüpfen, da es keinen vorherigen Abschnitt gibt.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Alle Kopf-/Fußzeilen des zweiten Abschnitts sind mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Im dritten Abschnitt ist nur die Fußzeile über den zweiten Abschnitt mit der Fußzeile des ersten Abschnitts verknüpft.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Siehe auch

* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
