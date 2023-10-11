---
title: ParagraphFormat.Bidi
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft ab oder legt fest ob es sich um einen Absatz mit Schreibrichtung von rechts nach links handelt.
type: docs
weight: 50
url: /de/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Ruft ab oder legt fest, ob es sich um einen Absatz mit Schreibrichtung von rechts nach links handelt.

```csharp
public bool Bidi { get; set; }
```

### Bemerkungen

Wann`WAHR`, die Läufe und andere Inline-Objekte in diesem Absatz sind von rechts nach links angeordnet.

### Beispiele

Zeigt, wie die Textrichtung eines Klartextdokuments erkannt wird.

```csharp
// Erstelle ein „TxtLoadOptions“-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft „DocumentDirection“ auf „DocumentDirection.Auto“ automatisch erkennt
// die Richtung jedes Textabsatzes, den Aspose.Words aus Klartext lädt.
// Die „Bidi“-Eigenschaft jedes Absatzes speichert seine Richtung.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Hebräischen Text als von rechts nach links geschrieben erkennen.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Englischen Text als von rechts nach links geschrieben erkennen.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Zeigt, wie man mit BIDIOUTLINE-Feldern sprachkompatible Listen mit der Schreibrichtung von rechts nach links erstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Das BIDIOUTLINE-Feld nummeriert Absätze wie die AUTONUM/LISTNUM-Felder,
// ist aber nur sichtbar, wenn eine Bearbeitungssprache von rechts nach links aktiviert ist, z. B. Hebräisch oder Arabisch.
// Das folgende Feld zeigt „.1“ an, das RTL-Äquivalent der Listennummer „1.“
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Zwei weitere BIDIOUTLINE-Felder hinzufügen, die „.2“ und „.3“ anzeigen.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Setzen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Wenn wir in Microsoft Word eine Bearbeitungssprache von rechts nach links aktivieren, werden in unseren Feldern Zahlen angezeigt.
// Andernfalls wird „###“ angezeigt.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


