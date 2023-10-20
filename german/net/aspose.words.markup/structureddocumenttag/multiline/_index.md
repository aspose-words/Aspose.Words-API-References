---
title: StructuredDocumentTag.Multiline
linktitle: Multiline
articleTitle: Multiline
second_title: Aspose.Words für .NET
description: StructuredDocumentTag Multiline eigendom. Gibt an ob dies der Fall istSDT Ermöglicht mehrere Textzeilen in C#.
type: docs
weight: 210
url: /de/net/aspose.words.markup/structureddocumenttag/multiline/
---
## StructuredDocumentTag.Multiline property

Gibt an, ob dies der Fall ist**SDT** Ermöglicht mehrere Textzeilen.

```csharp
public bool Multiline { get; set; }
```

## Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürRichText UndPlainText SDT-Typ.

Bei allen anderen SDT-Typen tritt eine Ausnahme auf.

## Beispiele

Zeigt, wie man ein strukturiertes Dokument-Tag in einem Nur-Text-Feld erstellt und sein Erscheinungsbild ändert.

```csharp
Document doc = new Document();

// Erstellen Sie ein strukturiertes Dokument-Tag, das einfachen Text enthält.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Legen Sie den Titel und die Farbe des Rahmens fest, der angezeigt wird, wenn Sie mit der Maus über das strukturierte Dokument-Tag in Microsoft Word fahren.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Legen Sie ein Tag für dieses strukturierte Dokument-Tag fest, das verfügbar ist
// als XML-Element mit dem Namen „tag“, mit der folgenden Zeichenfolge in seinem „@val“-Attribut.
tag.Tag = "MyPlainTextSDT";

// Jedes strukturierte Dokument-Tag hat eine zufällige eindeutige ID.
Assert.That(tag.Id, Is.Positive);

// Legen Sie die Schriftart für den Text innerhalb des strukturierten Dokument-Tags fest.
tag.ContentsFont.Name = "Arial";

// Legen Sie die Schriftart für den Text am Ende des strukturierten Dokument-Tags fest.
// Jeder Text, den wir in den Dokumentkörper eingeben, nachdem wir ihn mit den Pfeiltasten aus dem Tag herausbewegt haben, verwendet diese Schriftart.
tag.EndCharacterFont.Name = "Arial Black";

// Standardmäßig ist dies falsch und das Drücken der Eingabetaste innerhalb eines strukturierten Dokument-Tags führt zu nichts.
// Wenn es auf „true“ gesetzt ist, kann unser strukturiertes Dokument-Tag mehrere Zeilen haben.

// Setzen Sie die Eigenschaft „Multiline“ auf „false“, um nur den Inhalt zuzulassen
// dieses strukturierten Dokument-Tags, um eine einzelne Zeile zu umfassen.
// Setzen Sie die Eigenschaft „Multiline“ auf „true“, damit das Tag mehrere Zeilen Inhalt enthalten kann.
tag.Multiline = true;

// Setzen Sie die Eigenschaft „Appearance“ auf „SdtAppearance.Tags“, um Tags rund um den Inhalt anzuzeigen.
 // Standardmäßig wird das strukturierte Dokument-Tag als BoundingBox angezeigt.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Einen Klon unseres strukturierten Dokument-Tags in einen neuen Absatz einfügen.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Verwenden Sie die Methode „RemoveSelfOnly“, um ein strukturiertes Dokument-Tag zu entfernen und gleichzeitig seinen Inhalt im Dokument zu behalten.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
