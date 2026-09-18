---
title: "Aspose::Words::HeaderFooter::HeaderFooter Konstruktor"
linktitle: "HeaderFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HeaderFooter::HeaderFooter Konstruktor. Erstellt einen neuen Header oder eine neue Fußzeile des angegebenen Typs in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


Erstellt einen neuen Kopf- oder Fußzeilenbereich des angegebenen Typs.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
| headerFooterType | Aspose::Words::HeaderFooterType | Ein [HeaderFooterType](../get_headerfootertype/) Wert, der den Typ des Headers oder der Fußzeile angibt. |
## Hinweise


Wenn [HeaderFooter](../) erstellt wird, gehört es zum angegebenen Dokument, ist jedoch noch nicht Teil des Dokuments und [ParentNode](../../node/get_parentnode/) ist **null**.

Um [HeaderFooter](../) an einen [Section](../../section/) anzuhängen, verwenden Sie [InsertAfter1()</see>, <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../), oder die [HeadersFooters](../../section/get_headersfooters/) Eigenschaft und die Methoden [Add()](../), [Insert()](../).

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

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
