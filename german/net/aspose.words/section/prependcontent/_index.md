---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihren Inhalt mit der Methode „Section PrependContent“, indem Sie mühelos Quellabschnittstext am Anfang einfügen und so für mehr Organisation und Klarheit sorgen.
type: docs
weight: 160
url: /de/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

Fügt am Anfang dieses Abschnitts eine Kopie des Inhalts des Quellabschnitts ein.

```csharp
public void PrependContent(Section sourceSection)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceSection | Section | Der Abschnitt, aus dem Inhalte kopiert werden sollen. |

## Bemerkungen

Nur Inhalte von[`Body`](../body/) des Quellabschnitts wird kopiert, Seiteneinrichtung, Kopf- und Fußzeilen werden nicht kopiert.

Die Knoten werden automatisch importiert, wenn der Quellabschnitt zu einem anderen Dokument gehört.

Im Zieldokument wird kein neuer Abschnitt erstellt.

## Beispiele

Zeigt, wie der Inhalt eines Abschnitts an einen anderen Abschnitt angehängt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

// Den Inhalt des ersten Abschnitts am Anfang des dritten Abschnitts einfügen.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Den Inhalt des zweiten Abschnitts am Ende des dritten Abschnitts einfügen.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// Die Methoden „PrependContent“ und „AppendContent“ haben keine neuen Abschnitte erstellt.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
