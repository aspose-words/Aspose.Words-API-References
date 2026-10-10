---
title: "Aspose::Words::ParagraphAlignment enum"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphAlignment‑Enum. Gibt die Textausrichtung in einem Absatz in C++ an."
type: docs
weight: 110000
url: /de/cpp/aspose.words/paragraphalignment/
---
## ParagraphAlignment enum


Gibt die Textausrichtung in einem Absatz an.

```cpp
enum class ParagraphAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Links | 0 | Der Text ist linksbündig ausgerichtet. |
| Mitte | 1 | Der Text ist horizontal zentriert. |
| Rechts | 2 | Der Text ist rechtsbündig ausgerichtet. |
| Blocksatz | 3 | Der Text ist links- und rechtsbündig ausgerichtet. |
| Distributed | 4 | Der Text ist gleichmäßig verteilt. |
| ArabicMediumKashida | 5 | Nur Arabisch. Die Kashida-Länge für den Text wird auf eine mittlere Länge erweitert, die vom Verbraucher bestimmt wird. |
| ArabicHighKashida | 7 | Nur Arabisch. Die Kashida-Länge für den Text wird auf die größtmögliche Länge erweitert. |
| ArabicLowKashida | 8 | Nur Arabisch. Die Kashida-Länge für Text ist auf eine etwas längere Länge erweitert. |
| ThaiDistributed | 9 | Nur Thailändisch. Der Text wird mit einer Optimierung für Thailändisch ausgerichtet. |
| MathElementCenterAsGroup | 10 | Das einzige [Math](../../aspose.words.math/) Element in einer Zeile, ausgerichtet als 'Centered As Group'. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
