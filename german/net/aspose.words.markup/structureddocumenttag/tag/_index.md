---
title: StructuredDocumentTag.Tag
linktitle: Tag
articleTitle: Tag
second_title: Aspose.Words für .NET
description: Entdecken Sie die StructuredDocumentTag-Eigenschaft, die wichtige Tags für SDT-Knoten definiert und so eine effiziente Dokumentenverwaltung und -organisation gewährleistet.
type: docs
weight: 280
url: /de/net/aspose.words.markup/structureddocumenttag/tag/
---
## StructuredDocumentTag.Tag property

Gibt ein Tag an, das mit dem aktuellen SDT-Knoten verknüpft ist. Kann nicht`null` .

```csharp
public string Tag { get; set; }
```

## Bemerkungen

Ein Tag ist eine beliebige Zeichenfolge, die Anwendungen mit SDT verknüpfen können, um es zu identifizieren, ohne einen sichtbaren Anzeigenamen bereitzustellen.

## Beispiele

Zeigt, wie Sie in einem einfachen Textfeld ein strukturiertes Dokument-Tag erstellen und dessen Erscheinungsbild ändern.

```csharp
Document doc = new Document();

// Erstellen Sie ein strukturiertes Dokument-Tag, das einfachen Text enthält.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Legen Sie den Titel und die Farbe des Rahmens fest, der angezeigt wird, wenn Sie in Microsoft Word mit der Maus über das strukturierte Dokument-Tag fahren.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Setzen Sie ein Tag für dieses strukturierte Dokument-Tag, das erhältlich ist
// als XML-Element mit dem Namen „tag“, mit der folgenden Zeichenfolge im Attribut „@val“.
tag.Tag = "MyPlainTextSDT";

// Jedes strukturierte Dokument-Tag hat eine zufällige eindeutige ID.
Assert.IsTrue(tag.Id > 0);

// Legen Sie die Schriftart für den Text innerhalb des strukturierten Dokument-Tags fest.
tag.ContentsFont.Name = "Arial";

// Legen Sie die Schriftart für den Text am Ende des strukturierten Dokument-Tags fest.
// Jeder Text, den wir in den Dokumenttext eingeben, nachdem wir das Tag mit den Pfeiltasten verlassen haben, verwendet diese Schriftart.
tag.EndCharacterFont.Name = "Arial Black";

// Standardmäßig ist dies „false“ und das Drücken der Eingabetaste innerhalb eines strukturierten Dokument-Tags bewirkt nichts.
// Wenn auf „true“ gesetzt, kann unser strukturiertes Dokument-Tag mehrere Zeilen haben.

// Setzen Sie die Eigenschaft "Multiline" auf "false", um nur den Inhalt zuzulassen
// dieses strukturierten Dokument-Tags, um eine einzelne Zeile zu umfassen.
// Setzen Sie die Eigenschaft „Multiline“ auf „true“, damit das Tag mehrere Inhaltszeilen enthalten kann.
tag.Multiline = true;

// Setzen Sie die Eigenschaft „Darstellung“ auf „SdtAppearance.Tags“, um Tags um den Inhalt herum anzuzeigen.
    // Standardmäßig wird das strukturierte Dokument-Tag als BoundingBox angezeigt.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Fügen Sie einen Klon unseres strukturierten Dokument-Tags in einen neuen Absatz ein.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Verwenden Sie die Methode „RemoveSelfOnly“, um ein strukturiertes Dokument-Tag zu entfernen und gleichzeitig seinen Inhalt im Dokument beizubehalten.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
