---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.FontInfoCollection, Ihre Lösung für die effiziente Verwaltung von Dokumentschriftarten und die Verbesserung der visuellen Attraktivität Ihres Dokuments.
type: docs
weight: 3360
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
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Gibt an, ob Systemschriftarten in das Dokument eingebettet werden sollen oder nicht. Der Standardwert für diese Eigenschaft ist`FALSCH`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Gibt an, ob TrueType-Schriftarten beim Speichern in ein Dokument eingebettet werden sollen. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Ruft eine Schriftart mit dem angegebenen Namen ab. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Gibt an, ob eine Teilmenge der eingebetteten TrueType-Schriftarten mit dem Dokument gespeichert werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH`. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Bestimmt, ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |

## Bemerkungen

Artikel sind[`FontInfo`](../fontinfo/) Objekte.

Sie erstellen keine Instanzen dieser Klasse direkt. Verwenden Sie die[`FontInfos`](../../aspose.words/documentbase/fontinfos/) -Eigenschaft, um auf die im Dokument definierte Schriftartensammlung zuzugreifen.

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

Zeigt, wie Sie die Details der in einem Dokument vorhandenen Schriftarten ausdrucken.

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

### Siehe auch

* class [FontInfo](../fontinfo/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)
