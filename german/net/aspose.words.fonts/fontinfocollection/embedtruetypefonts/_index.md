---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie die Eigenschaft EmbedTrueTypeFonts in FontInfoCollection die Dokumentqualität durch die Einbettung von TrueType-Schriftarten verbessert. Der Standardwert ist „false“.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Gibt an, ob TrueType-Schriftarten beim Speichern in ein Dokument eingebettet werden sollen. Der Standardwert für diese Eigenschaft ist`FALSCH` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Bemerkungen

Durch das Einbetten von TrueType-Schriftarten können andere das Dokument mit denselben Schriftarten anzeigen, die zum Erstellen verwendet wurden. Die Dokumentgröße kann sich dadurch jedoch erheblich erhöhen.

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
