---
title: "Aspose::Words::Run::Run Konstruktor"
linktitle: "Lauf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Run::Run-Konstruktor. Initialisiert eine neue Instanz der Run-Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/run/run/
---
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initialisiert eine neue Instanz der [Run](../)-Klasse.

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
## Hinweise


Wenn [Run](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und [ParentNode](../../node/get_parentnode/) ist **null**.

Um [Run](../) an das Dokument anzuhängen, verwenden Sie [InsertAfter1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) im Absatz, in dem Sie den Run einfügen möchten.

## Beispiele



Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
// Rufen Sie die Methode "RemoveAllChildren" auf, um alle diese Knoten zu entfernen,
// und erhalten ein Dokumentenknoten ohne Kinder.
doc->RemoveAllChildren();

// Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
// Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
// Erstellen Sie zunächst einen neuen Abschnitt und fügen Sie ihn dann als Kind zum Wurzel-Dokumentenknoten hinzu.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt.
// auf der Seite zwischen der Kopf‑ und Fußzeile des Abschnitts.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Fügen Sie schließlich etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
// setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Run::Run(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) constructor


Initialisiert eine neue Instanz der Klasse **Run**.

```cpp
Aspose::Words::Run::Run(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &text)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
| Text | const System::String\& | Der Text des Runs. |
## Hinweise


Wenn [Run](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und [ParentNode](../../node/get_parentnode/) ist **null**.

Um [Run](../) an das Dokument anzuhängen, verwenden Sie [InsertAfter1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) im Absatz, in dem Sie den Run einfügen möchten.

## Beispiele



Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
