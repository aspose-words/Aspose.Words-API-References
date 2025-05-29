---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveSubsetFonts-Eigenschaft der FontInfoCollection und steuern Sie eingebettete TrueType-Schriftarten-Teilmengen in Ihren Dokumenten, um Dateigröße und Leistung zu optimieren.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Gibt an, ob eine Teilmenge der eingebetteten TrueType-Schriftarten mit dem Dokument gespeichert werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH`.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../embedtruetypefonts/) Eigenschaft ist auf`WAHR`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Bemerkungen

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

## Beispiele

Zeigt, wie ein Dokument mit eingebetteten TrueType-Schriftarten gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Siehe auch

* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
