---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words für .NET
description: Entdecken Sie die FindReplaceOptions-Eigenschaft „IgnoreStructuredDocumentTags“. Steuern Sie mit dieser benutzerfreundlichen booleschen Einstellung, ob StructuredDocumentTag-Inhalte ignoriert werden.
type: docs
weight: 120
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Ruft einen booleschen Wert ab oder setzt ihn, der angibt, ob der Inhalt von[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## Bemerkungen

Wenn diese Option auf`WAHR` , der Inhalt von[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) wird als einfacher Text behandelt.

Andernfalls[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) wird als eigenständige Story verarbeitet und das ersetzende Muster wird für jede[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , , so dass, wenn das Muster ein[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , dann wird für dieses Muster kein Ersatz durchgeführt.

## Beispiele

Zeigt, wie der Inhalt von Tags beim Ersetzen ignoriert wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Dieser Absatz enthält SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
