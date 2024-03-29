---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Erhält oder setzt einen Wert der festlegt welche Dokumentformate abgebildet werden dürfenXmlMapping . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden.
type: docs
weight: 90
url: /de/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Bemerkungen

Diese Option ist gepaart mit[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . In der Regel müssen Sie beide auf „false“ setzen, damit beliebige Dokumentformate zugeordnet werden können.

### Beispiele

Zeigt, wie strukturierte Dokument-Tags an ein beliebiges Format gebunden werden.

```csharp
// Wenn wahr - SDT enthält rohen HTML-Text.
// Wenn falsch - wird gemapptes HTML geparst und das resultierende Dokument wird in den SDT-Inhalt eingefügt.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


