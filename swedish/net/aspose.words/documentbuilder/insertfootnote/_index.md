---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder InsertFootnote-metoden – lägg enkelt till fotnoter eller slutnoter för ökad tydlighet och professionalism.
type: docs
weight: 340
url: /sv/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Infogar en fotnot eller slutnot i dokumentet.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| footnoteType | FootnoteType | Anger om en fotnot eller en slutnot ska infogas. |
| footnoteText | String | Anger texten i fotnoten. |

### Returvärde

Returnerar ett fotnotsobjekt som just skapades.

## Exempel

Visar hur man refererar till text med en fotnot och en slutnot.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga lite text och markera den med en fotnot med IsAuto-egenskapen inställd på "true" som standard,
// så markören som syns i brödtexten kommer att automatiskt numreras vid "1",
// och fotnoten kommer att visas längst ner på sidan.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Infoga mer text och markera den med en slutnot med ett anpassat referensmärke,
// som kommer att användas istället för siffran "2" och sätta "IsAuto" till falskt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fotnoter visas alltid längst ner i den refererade texten,
// så denna sidbrytning kommer inte att påverka fotnoten.
// Å andra sidan finns slutnoter alltid i slutet av dokumentet
// så att denna sidbrytning flyttar slutnoten ner till nästa sida.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Se även

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Infogar en fotnot eller slutnot i dokumentet.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| footnoteType | FootnoteType | Anger om en fotnot eller en slutnot ska infogas. |
| footnoteText | String | Anger texten i fotnoten. |
| referenceMark | String | Anger fotnotens anpassade referensmärke. |

### Returvärde

Returnerar ett fotnotsobjekt som just skapades.

## Exempel

Visar hur man refererar till text med en fotnot och en slutnot.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga lite text och markera den med en fotnot med IsAuto-egenskapen inställd på "true" som standard,
// så markören som syns i brödtexten kommer att automatiskt numreras vid "1",
// och fotnoten kommer att visas längst ner på sidan.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Infoga mer text och markera den med en slutnot med ett anpassat referensmärke,
// som kommer att användas istället för siffran "2" och sätta "IsAuto" till falskt.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Fotnoter visas alltid längst ner i den refererade texten,
// så denna sidbrytning kommer inte att påverka fotnoten.
// Å andra sidan finns slutnoter alltid i slutet av dokumentet
// så att denna sidbrytning flyttar slutnoten ner till nästa sida.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Se även

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
