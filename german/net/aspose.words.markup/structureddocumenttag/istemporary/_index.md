---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „StructuredDocumentTag IsTemporary“ bestimmt, ob Ihr SDT bei Inhaltsänderungen aus WordProcessingML entfernt wird. Optimieren Sie Ihre Dokumente noch heute!
type: docs
weight: 160
url: /de/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Gibt an, ob diese**SDT** soll aus dem WordProcessingML-Dokument entfernt werden, wenn sein Inhalt geändert wird.

```csharp
public bool IsTemporary { get; set; }
```

## Beispiele

Zeigt, wie man Einwegkontrollen herstellt.

```csharp
Document doc = new Document();

// Fügen Sie ein Dokument-Tag mit einfacher Textstruktur ein.
// das als reines Textformular fungiert, in das der Benutzer Text eingeben kann.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Setzen Sie die Eigenschaft "IsTemporary" auf "true", damit das strukturierte Dokument-Tag verschwindet und
// seinen Inhalt in das Dokument integrieren, nachdem der Benutzer ihn einmal in Microsoft Word bearbeitet hat.
// Setzen Sie die Eigenschaft „IsTemporary“ auf „false“, um dem Benutzer das Bearbeiten des Inhalts zu ermöglichen
// des strukturierten Dokument-Tags beliebig oft.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Fügen Sie ein weiteres strukturiertes Dokument-Tag in Form eines Kontrollkästchens ein und setzen Sie seinen Standardstatus auf „aktiviert“.
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Setzen Sie die Eigenschaft „IsTemporary“ auf „true“, um das Kontrollkästchen zu einem Symbol zu machen
// sobald der Benutzer in Microsoft Word darauf klickt.
// Setzen Sie die Eigenschaft „IsTemporary“ auf „false“, um dem Benutzer zu ermöglichen, beliebig oft auf das Kontrollkästchen zu klicken.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
