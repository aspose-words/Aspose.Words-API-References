---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words für .NET
description: FontInfoCollection EmbedSystemFonts eigendom. Gibt an ob Systemschriftarten in das Dokument eingebettet werden sollen. Der Standardwert für diese Eigenschaft istFALSCH in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen. Der Standardwert für diese Eigenschaft ist`FALSCH`.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../embedtruetypefonts/) Option ist auf eingestellt`WAHR`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Bemerkungen

Diese Eigenschaft festlegen auf`WAHR`ist nützlich, wenn der Benutzer ein ostasiatisches System verwendet und ein Dokument erstellen möchte, das für andere lesbar ist, die keine Schriftarten für diese -Sprache auf ihrem System haben. Beispielsweise könnte ein Benutzer auf einem japanischen System die -Schriftarten in ein Dokument einbetten, sodass das japanische Dokument auf allen Systemen lesbar wäre.

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

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Siehe auch

* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
