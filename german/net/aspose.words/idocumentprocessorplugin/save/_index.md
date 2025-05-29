---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words für .NET
description: Speichern Sie Dokumente mühelos mit der IDocumentProcessorPlugin-Speichermethode und gewährleisten Sie eine optimale Ausgabe mit anpassbaren Speicheroptionen für Ihre Anforderungen.
type: docs
weight: 30
url: /de/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Speichern Sie das geladene Dokument von[`Load`](../load/) Methode zum Ausgabestream unter Verwendung der angegebenen Speicheroptionen.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Der Ausgabestream. |
| saveOptions | SaveOptions | Die Speicheroptionen. |

## Bemerkungen

Wenn das angegebene Ausgabeformat Bild ist, wird nur das Bild der ersten Seite im Ausgabestream gespeichert. Wenn das angegebene Speicherformat nicht nativ vom Plugin unterstützt wird (erfordert das Laden in[`Document`](../../document/)), -Methode löst eine Ausnahme aus.

### Siehe auch

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
