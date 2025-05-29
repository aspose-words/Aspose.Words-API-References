---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die FontInfoCollection-Eigenschaft EmbedSystemFonts Ihre Dokumente durch die Einbettung von Systemschriften verbessert. Erfahren Sie mehr über den Standardwert und die Vorteile!
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist`FALSCH`.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../embedtruetypefonts/) ist auf`WAHR`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Bemerkungen

Festlegen dieser Eigenschaft auf`WAHR` Dies ist nützlich, wenn der Benutzer ein ostasiatisches System verwendet und ein Dokument erstellen möchte, das auch von anderen Benutzern gelesen werden kann, die keine Schriftarten für diese Sprache auf ihrem System installiert haben. Beispielsweise könnte ein Benutzer eines japanischen Systems die Schriftarten in ein Dokument einbetten, sodass das japanische Dokument auf allen Systemen lesbar ist.

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
