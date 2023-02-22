---
title: SaveOptions.UpdateSdtContent
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Erhält oder setzt den Wert der bestimmt ob der Inhalt vonStructuredDocumentTag wird vor dem Speichern aktualisiert.
type: docs
weight: 200
url: /de/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

Erhält oder setzt den Wert, der bestimmt, ob der Inhalt von[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) wird vor dem Speichern aktualisiert.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Bemerkungen

Der Standardwert ist`Stimmt` .

### Beispiele

Zeigt, wie strukturierte Dokument-Tags aktualisiert werden, während ein Dokument als PDF gespeichert wird.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Dokument-Tag aus einer Dropdown-Liste ein.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// Die Dropdown-Liste zeigt derzeit "Choose an item" als Standardtext an.
// Setzen Sie die "SelectedValue"-Eigenschaft auf eines der Listenelemente, um das Tag zu erhalten
// Den Wert dieses Listenelements anstelle des Standardtexts anzeigen.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das an die "Save"-Methode des Dokuments übergeben wird
// um zu ändern, wie diese Methode das Dokument in .PDF speichert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „UpdateSdtContent“ auf „false“, um die Tags des strukturierten Dokuments nicht zu aktualisieren
// beim Speichern des Dokuments als PDF. Sie zeigen ihre Standardwerte so an, wie sie zum Zeitpunkt der Konstruktion waren.
// Legen Sie die Eigenschaft "UpdateSdtContent" auf "true" fest, um sicherzustellen, dass die Tags aktualisierte Werte in der PDF-Datei anzeigen.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


