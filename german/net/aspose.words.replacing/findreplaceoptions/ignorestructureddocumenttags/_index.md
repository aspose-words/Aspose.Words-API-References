---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt ob der Inhalt ignoriert werden sollStructuredDocumentTag . Der Standardwert istFALSCH .
type: docs
weight: 120
url: /de/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob der Inhalt ignoriert werden soll[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

### Bemerkungen

Wenn diese Option auf eingestellt ist`WAHR` , der Inhalt von[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) wird als einfacher Text behandelt.

Ansonsten,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) wird als eigenständige Story verarbeitet und das ersetzende Muster wird für jedes separat gesucht[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), , so dass, wenn das Muster a kreuzt[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , dann wird für ein solches Muster keine Ersetzung durchgeführt.

### Beispiele

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
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


