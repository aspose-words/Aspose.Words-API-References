---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ParagraphFormat Bidi“, mit der Sie die Textformatierung von rechts nach links einfach steuern und so die Lesbarkeit und das Dokumentlayout verbessern können.
type: docs
weight: 50
url: /de/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Ruft ab oder legt fest, ob es sich um einen von rechts nach links verlaufenden Absatz handelt.

```csharp
public bool Bidi { get; set; }
```

## Bemerkungen

Wann`WAHR`, die Läufe und anderen Inline-Objekte in diesem Absatz werden von rechts nach links angeordnet.

## Beispiele

Zeigt, wie die Textrichtung in Klartextdokumenten erkannt wird.

```csharp
// Erstelle ein "TxtLoadOptions"-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft "DocumentDirection" auf "DocumentDirection.Auto" erkennt automatisch
// die Richtung jedes Textabsatzes, den Aspose.Words aus dem Klartext lädt.
// Die „Bidi“-Eigenschaft jedes Absatzes speichert seine Richtung.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Hebräischen Text als von rechts nach links lesend erkennen.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Englischen Text als von rechts nach links lesend erkennen.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Zeigt, wie man mit BIDIOUTLINE-Feldern sprachkompatible Listen von rechts nach links erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das Feld BIDIOUTLINE nummeriert Absätze wie die Felder AUTONUM/LISTNUM,
// ist aber nur sichtbar, wenn eine von rechts nach links geschriebene Bearbeitungssprache aktiviert ist, beispielsweise Hebräisch oder Arabisch.
// Das folgende Feld zeigt „.1“ an, das RTL-Äquivalent der Listennummer „1.“.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Fügen Sie zwei weitere BIDIOUTLINE-Felder hinzu, die „.2“ und „.3“ anzeigen.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Stellen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL ein.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Wenn wir in Microsoft Word eine Bearbeitungssprache mit Schreibrichtung von rechts nach links aktivieren, werden in unseren Feldern Zahlen angezeigt.
// Andernfalls wird „###“ angezeigt.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
