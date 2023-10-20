---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: Aspose.Words för .NET
description: Section PrependContent metod. Infogar en kopia av innehållet i källavsnittet i början av det här avsnittet i C#.
type: docs
weight: 140
url: /sv/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

Infogar en kopia av innehållet i källavsnittet i början av det här avsnittet.

```csharp
public void PrependContent(Section sourceSection)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceSection | Section | Avsnittet att kopiera innehåll från. |

## Anmärkningar

Endast innehållet i[`Body`](../body/) av källsektionen kopieras, sidinställningar, sidhuvuden och sidfötter kopieras inte.

Noderna importeras automatiskt om källdelen tillhör ett annat dokument.

Ingen ny sektion skapas i måldokumentet.

## Exempel

Visar hur man lägger till innehållet i ett avsnitt till ett annat avsnitt.

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

// Infoga innehållet i det första avsnittet i början av det tredje avsnittet.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// Infoga innehållet i det andra avsnittet i slutet av det tredje avsnittet.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// Metoderna "PrependContent" och "AppendContent" skapade inga nya sektioner.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
