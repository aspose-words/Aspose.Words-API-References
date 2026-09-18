---
title: "Aspose::Words::Node::get_ParentNode Methode"
linktitle: "get_ParentNode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::get_ParentNode Methode. Gibt den unmittelbaren Elternknoten dieses Knotens in C++ zurück."
type: docs
weight: 10000
url: /de/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Ermittelt den unmittelbaren Elternknoten dieses Knotens.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Hinweise


Wenn ein Knoten gerade erst erstellt wurde und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde, ist der Elternknoten **null**.

## Beispiele



Zeigt, wie man auf den Elternknoten eines Knotens zugreift.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Fügen Sie einen untergeordneten Run‑Knoten zum ersten Absatz des Dokuments hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Der Absatz ist der Elternknoten des Run‑Knotens. Wir können diese Herkunft nachverfolgen
// bis zum Dokumentknoten, der die Wurzel des Knotensbaums des Dokuments ist.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


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

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
