---
title: Class FontInfoCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontInfoCollection klas. Stellt eine Sammlung von Schriftarten dar die in einem Dokument verwendet werden.
type: docs
weight: 2930
url: /de/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Stellt eine Sammlung von Schriftarten dar, die in einem Dokument verwendet werden.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen. Der Standardwert für diese Eigenschaft ist`FALSCH`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Gibt an, ob TrueType-Schriftarten beim Speichern in ein Dokument eingebettet werden sollen. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Ruft eine Schriftart mit dem angegebenen Namen ab. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Gibt an, ob eine Teilmenge der eingebetteten TrueType-Schriftarten mit document. gespeichert werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH`. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(string) | Ermittelt, ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |

### Bemerkungen

Artikel sind[`FontInfo`](../fontinfo/) Objekte.

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`FontInfos`](../../aspose.words/documentbase/fontinfos/) Eigenschaft, um auf die im Dokument definierte Sammlung von Schriftarten zuzugreifen.

### Beispiele

Zeigt, wie die Details zu den in einem Dokument vorhandenen Schriftarten gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Alle verwendeten und nicht verwendeten Schriftarten im Dokument drucken.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfo](../fontinfo/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


