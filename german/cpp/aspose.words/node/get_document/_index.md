---
title: "Aspose::Words::Node::get_Document-Methode"
linktitle: "get_Document"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::get_Document Methode. Ermittelt das Dokument, zu dem dieser Knoten in C++ gehört."
type: docs
weight: 6000
url: /de/cpp/aspose.words/node/get_document/
---
## Node::get_Document method


Ermittelt das Dokument, zu dem dieser Knoten gehört.

```cpp
virtual System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Node::get_Document() const
```

## Hinweise


Der Knoten gehört immer zu einem Dokument, selbst wenn er gerade erst erstellt wurde und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde.

## Beispiele



Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Wir haben diesen Absatz noch nicht als Kind zu einem zusammengesetzten Knoten hinzugefügt.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Wenn ein Knoten ein geeigneter Kindknotentyp eines anderen zusammengesetzten Knotens ist,
// können wir ihn nur dann als Kind anhängen, wenn beide Knoten dasselbe Eigentümerdokument haben.
// Das Eigentümerdokument ist das Dokument, das wir dem Konstruktor des Knotens übergeben haben.
// Wir haben diesen Absatz nicht an das Dokument angehängt, daher enthält das Dokument seinen Text nicht.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Da das Dokument diesen Absatz besitzt, können wir einen seiner Stile auf den Inhalt des Absatzes anwenden.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Fügen Sie diesen Knoten dem Dokument hinzu und überprüfen Sie anschließend dessen Inhalt.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
