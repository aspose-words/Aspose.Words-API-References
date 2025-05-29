---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Layout.RevisionColor-uppräkningen för att anpassa dokumentrevisionsfärger, förbättra tydligheten och samarbetet i dina dokument.
type: docs
weight: 3830
url: /sv/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Gör det möjligt att ange färgen på dokumentrevisioner.

```csharp
public enum RevisionColor
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Standard. |
| Black | `1` | Representerar färgen 000000. |
| Blue | `2` | Representerar färgen 2e97d3. |
| BrightGreen | `3` | Representerar färgen 84a35b. |
| ClassicBlue | `4` | Representerar 0000ff färg. |
| ClassicRed | `5` | Representerar färgen ff0000. |
| DarkBlue | `6` | Representerar färgen 376e96. |
| DarkRed | `7` | Representerar färgen 881824. |
| DarkYellow | `8` | Representerar färgen e09a2b. |
| Gray25 | `9` | Representerar färgen a0a3a9. |
| Gray50 | `10` | Representerar färgen 50565e. |
| Green | `11` | Representerar färgen 2c6234. |
| Pink | `12` | Representerar ce338f färg. |
| Red | `13` | Representerar färgen b5082e. |
| Teal | `14` | Representerar 1b9cab-färgen. |
| Turquoise | `15` | Representerar färgen 3eafc2. |
| Violet | `16` | Representerar färgen 633277. |
| White | `17` | Representerar färgen ffffff. |
| Yellow | `18` | Representerar färgen fad272. |
| LightPink | `19` | Representerar färgen fce6f4. |
| LightBlue | `20` | Representerar färgen e1f2fa. |
| LightYellow | `21` | Representerar fef4de-färgen. |
| LightPurple | `22` | Representerar eadfef-färg. |
| LightOrange | `23` | Representerar färgen fce3d0. |
| LightGreen | `24` | Representerar e9f8ce-färgen. |
| Gray | `25` | Representerar en federerad färg. |
| NoHighlight | `26` | Ingen färg används för att markera revisionsändringar. |
| ByAuthor | `27` | Revisioner av varje författare får sin egen färg för att markeras från en fördefinierad uppsättning högkontrastfärger. |

## Exempel

Visar hur man ändrar utseendet på revisioner i ett renderat utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en revision och ändra sedan färgen på alla revisioner till grön.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Ta bort fältet som visas till vänster om varje reviderad rad.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
