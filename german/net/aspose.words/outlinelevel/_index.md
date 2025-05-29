---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.OutlineLevel, um die Gliederungsebenen von Absätzen in Ihren Dokumenten einfach zu verwalten und so für mehr Ordnung und Übersichtlichkeit zu sorgen.
type: docs
weight: 5060
url: /de/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Gibt die Gliederungsebene eines Absatzes im Dokument an.

```csharp
public enum OutlineLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Level1 | `0` | Der Absatz befindet sich auf Gliederungsebene 1 (oberste Ebene). |
| Level2 | `1` | Der Absatz befindet sich auf Gliederungsebene 2. |
| Level3 | `2` | Der Absatz befindet sich auf Gliederungsebene 3. |
| Level4 | `3` | Der Absatz befindet sich auf Gliederungsebene 4. |
| Level5 | `4` | Der Absatz befindet sich auf Gliederungsebene 5. |
| Level6 | `5` | Der Absatz befindet sich auf Gliederungsebene 6. |
| Level7 | `6` | Der Absatz befindet sich auf Gliederungsebene 7. |
| Level8 | `7` | Der Absatz befindet sich auf Gliederungsebene 8. |
| Level9 | `8` | Der Absatz befindet sich auf Gliederungsebene 9. |
| BodyText | `9` | Der Absatz befindet sich auf der Ebene des Haupttextes. |

## Beispiele

Zeigt, wie Sie Absatzgliederungsebenen konfigurieren, um reduzierbaren Text zu erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz hat einen OutlineLevel, der eine beliebige Zahl zwischen 1 und 9 oder der Standardwert „BodyText“ sein kann.
// Wenn Sie die Eigenschaft auf einen der nummerierten Werte setzen, wird ein Pfeil nach links angezeigt
// vom Anfang des Absatzes.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Ebene 1 ist die oberste Ebene. Wenn sich unter einem Absatz mit einer höheren Ebene ein Absatz mit einer niedrigeren Ebene befindet,
// Durch das Ausblenden des Absatzes auf höherer Ebene wird auch der Absatz auf niedrigerer Ebene ausgeblendet.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Zwei Absätze derselben Ebene werden nicht zusammenfallen,
// und die Pfeile klappen die Absätze, auf die sie zeigen, nicht zusammen.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Der Standardwert für „BodyText“ ist der niedrigste, um den ein Absatz jeder Ebene eingeklappt werden kann.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
