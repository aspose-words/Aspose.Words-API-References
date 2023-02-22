---
title: FontInfoCollection.EmbedSystemFonts
second_title: Aspose.Words für .NET-API-Referenz
description: FontInfoCollection eigendom. Gibt an ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist FALSCH.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist **FALSCH**.

Diese Option funktioniert nur, wenn[`EmbedTrueTypeFonts`](../embedtruetypefonts/) Option eingestellt ist **Stimmt**.

```csharp
public bool EmbedSystemFonts { get; set; }
```

### Bemerkungen

Setzen dieser Eigenschaft auf`WAHR`ist nützlich, wenn sich der Benutzer auf einem ostasiatischen System befindet und ein Dokument erstellen möchte, das von anderen gelesen werden kann, die keine Schriftarten für diese -Sprache auf ihrem System haben. Beispielsweise könnte ein Benutzer eines japanischen Systems die Schriftarten in ein Dokument einbetten, sodass das japanische Dokument auf allen Systemen lesbar wäre.

Diese Option funktioniert nur für die Formate DOC, DOCX und RTF.

### Beispiele

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
* namensraum [Aspose.Words.Fonts](../../fontinfocollection/)
* Montage [Aspose.Words](../../../)


