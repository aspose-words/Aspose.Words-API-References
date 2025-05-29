---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mühelos mit der InsertStructuredDocumentTag-Methode von DocumentBuilder. Fügen Sie einfach strukturierte Dokument-Tags hinzu, um die Organisation zu verbessern!
type: docs
weight: 480
url: /de/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Fügt ein[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) in das Dokument.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Rückgabewert

Der[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Knoten, der gerade eingefügt wurde.

## Beispiele

Zeigt, wie man einfach strukturierte Dokument-Tags einfügt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Beachten Sie, dass nur die folgenden StructuredDocumentTag-Typen eingefügt werden dürfen:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Bild, SdtType.Datum.
// Die Markup-Ebene des eingefügten StructuredDocumentTag wird automatisch erkannt und hängt von der Position ab, an der es eingefügt wird.
// Hinzugefügtes StructuredDocumentTag übernimmt Absatz- und Schriftformatierung von der Cursorposition.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
