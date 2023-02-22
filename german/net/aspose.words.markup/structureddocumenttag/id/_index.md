---
title: StructuredDocumentTag.Id
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag eigendom. Gibt eine eindeutige schreibgeschützte persistente numerische ID dafür an SDT.
type: docs
weight: 140
url: /de/net/aspose.words.markup/structureddocumenttag/id/
---
## StructuredDocumentTag.Id property

Gibt eine eindeutige, schreibgeschützte, persistente numerische ID dafür an **SDT**.

```csharp
public int Id { get; }
```

### Bemerkungen

Das ID-Attribut muss diesen Regeln folgen:

* Das Dokument behält SDT-IDs nur dann bei, wenn das gesamte Dokument geklont wird[`Clone`](../../../aspose.words/document/clone/).
* Während[`ImportNode`](../../../aspose.words/documentbase/importnode/) ID soll beibehalten werden, wenn der Import keine Konflikte mit anderen SDT-IDs in des Zieldokuments verursacht.
* Wenn mehrere SDT-Knoten denselben Dezimalzahlwert für das Id-Attribut spezifizieren, dann behält das erste SDT im Dokument diese ursprüngliche ID bei, und allen nachfolgenden SDT-Knoten werden neue Kennungen zugewiesen, wenn das Dokument geladen wird.
* Während des eigenständigen SDTINodeCloningListener) Vorgang wird eine neue eindeutige ID für den geklonten SDT-Knoten generiert.
* Wenn die ID im Quelldokument nicht angegeben ist, wird dem SDT-Knoten eine neue eindeutige Kennung zugewiesen , wenn das Dokument geladen wird.

### Beispiele

Zeigt, wie ein strukturiertes Dokument-Tag in einem Nur-Text-Feld erstellt und sein Erscheinungsbild geändert wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein strukturiertes Dokument-Tag, das einfachen Text enthält.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Legen Sie den Titel und die Farbe des Rahmens fest, der angezeigt wird, wenn Sie die Maus über das strukturierte Dokument-Tag in Microsoft Word bewegen.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Setzen Sie ein Tag für dieses strukturierte Dokument-Tag, das erhältlich ist
// als ein XML-Element mit dem Namen "tag", mit der unten stehenden Zeichenfolge in seinem "@val"-Attribut.
tag.Tag = "MyPlainTextSDT";

// Jedes strukturierte Dokument-Tag hat eine zufällige eindeutige ID.
Assert.That(tag.Id, Is.Positive);

// Legen Sie die Schriftart für den Text innerhalb des strukturierten Dokument-Tags fest.
tag.ContentsFont.Name = "Arial";

// Legen Sie die Schriftart für den Text am Ende des strukturierten Dokument-Tags fest.
// Jeder Text, den wir in den Textkörper des Dokuments eingeben, nachdem wir uns mit den Pfeiltasten aus dem Tag herausbewegt haben, verwendet diese Schriftart.
tag.EndCharacterFont.Name = "Arial Black";

// Standardmäßig ist dies falsch und das Drücken der Eingabetaste innerhalb eines strukturierten Dokument-Tags bewirkt nichts.
// Wenn es auf true gesetzt ist, kann unser strukturiertes Dokument-Tag mehrere Zeilen haben.

// Setzen Sie die Eigenschaft "Multiline" auf "false", um nur den Inhalt zuzulassen
// dieses strukturierten Dokument-Tags, um eine einzelne Zeile zu überspannen.
// Setzen Sie die Eigenschaft "Multiline" auf "true", damit das Tag mehrere Inhaltszeilen enthalten kann.
tag.Multiline = true;

// Legen Sie die Eigenschaft "Appearance" auf "SdtAppearance.Tags" fest, um Tags um den Inhalt herum anzuzeigen.
 // Standardmäßig wird das strukturierte Dokument-Tag als BoundingBox angezeigt.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Einen Klon unseres strukturierten Dokument-Tags in einen neuen Absatz einfügen.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Verwenden Sie die Methode "RemoveSelfOnly", um ein strukturiertes Dokument-Tag zu entfernen, während sein Inhalt im Dokument bleibt.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


