---
title: StructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „StructuredDocumentTag RemoveSelfOnly“, um mühelos einen SDT-Knoten zu entfernen und gleichzeitig dessen Inhalt im Dokument zu erhalten. Steigern Sie Ihre Bearbeitungseffizienz!
type: docs
weight: 370
url: /de/net/aspose.words.markup/structureddocumenttag/removeselfonly/
---
## StructuredDocumentTag.RemoveSelfOnly method

Entfernt nur diesen SDT-Knoten selbst, behält aber seinen Inhalt im Dokumentbaum.

```csharp
public void RemoveSelfOnly()
```

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
