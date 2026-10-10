---
title: "Aspose::Words::HeaderFooterCollection class"
linktitle: "HeaderFooterCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooterCollection class. Bietet typisierten Zugriff auf HeaderFooter-Knoten einer Section. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 32000
url: /de/cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


Bietet typisierten Zugriff auf [HeaderFooter](../headerfooter/) Knoten einer [Section](../section/). Weitere Informationen finden Sie im Dokumentationsartikel [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/).

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get_Count](../nodecollection/get_count/)() | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft ein [HeaderFooter](../headerfooter/) am angegebenen Index ab. |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | Ruft ein [HeaderFooter](../headerfooter/) des angegebenen Typs ab. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | Verknüpft oder löst alle Kopf- und Fußzeilen mit den entsprechenden Kopf- und Fußzeilen im vorherigen Abschnitt. |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | Verknüpft oder löst die angegebene Kopf- oder Fußzeile mit der entsprechenden Kopf- oder Fußzeile im vorherigen Abschnitt. |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](./toarray/)() | Kopiert alle **HeaderFooter**s aus der Sammlung in ein neues Array von **HeaderFooter**s. |
| static [Type](./type/)() |  |
## Hinweise


Es kann höchstens ein [HeaderFooter](../headerfooter/) geben.

von jedem [HeaderFooterType](../headerfootertype/) pro [Section](../section/).

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

## Beispiele



Zeigt, wie man eine Kopfzeile und eine Fußzeile erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle eine Kopfzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird oben auf jeder Seite dieses Abschnitts angezeigt, über dem Haupttext.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Erstelle eine Fußzeile und füge einen Absatz hinzu. Der Text in diesem Absatz
// wird unten auf jeder Seite dieses Abschnitts angezeigt, unter dem Haupttext.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


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

## Siehe auch

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
