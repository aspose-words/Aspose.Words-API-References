---
title: "Aspose::Words::HeaderFooterCollection::idx_get-Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooterCollection::idx_get-Methode. Ruft in C++ ein HeaderFooter des angegebenen Typs ab."
type: docs
weight: 3000
url: /de/cpp/aspose.words/headerfootercollection/idx_get/
---
## HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType) method


Ruft ein [HeaderFooter](../../headerfooter/) des angegebenen Typs ab.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Ein [HeaderFooterType](../../headerfootertype/)-Wert, der den Typ des abzurufenden Headers/Fußzeile angibt. |

## Beispiele



Zeigt, wie man alle Fußzeilen aus einem Dokument löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Iteriere durch jeden Abschnitt und entferne Fußzeilen aller Art.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Es gibt drei Arten von Fuß- und Kopfzeilentypen.
    // 1 -  Die \"Erste\" Kopf-/Fußzeile, die nur auf der ersten Seite eines Abschnitts erscheint.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  Die \"Primäre\" Kopf-/Fußzeile, die auf ungeraden Seiten erscheint.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  Die \"Gerade\" Kopf-/Fußzeile, die auf geraden Seiten erscheint.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Zeigt, wie man Text in der Fußzeile eines Dokuments ersetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Siehe auch

* Class [HeaderFooter](../../headerfooter/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::idx_get(int32_t) method


Ruft ein [HeaderFooter](../../headerfooter/) am angegebenen Index ab.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Sammlung. |
## Hinweise


Der Index ist nullbasiert.

Negative Indizes sind erlaubt und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer als oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer ist als die Anzahl der Elemente in der Liste, gibt dies eine Nullreferenz zurück.

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

* Class [HeaderFooter](../../headerfooter/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
