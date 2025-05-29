---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words für .NET
description: Vergleichen Sie Dokumente mühelos mit CompareToImages, indem Sie Unterschiede als Bilder für jede Seite speichern und so die Übersichtlichkeit und visuelle Analyse verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jedes Element im zurückgegebenen Array stellt eine einzelne Seite der als Bild gerenderten Ausgabe dar.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | String | Das Originaldokument. |
| v2 | String | Das geänderte Dokument. |
| imageSaveOptions | ImageSaveOptions | Die Bildspeicheroptionen der Ausgabe. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Vergleicht zwei Dokumente und speichert die Unterschiede als Bilder. Jedes Element im zurückgegebenen Array stellt eine einzelne Seite der als Bild gerenderten Ausgabe dar.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| v1 | Stream | Das Originaldokument. |
| v2 | Stream | Das geänderte Dokument. |
| imageSaveOptions | ImageSaveOptions | Die Bildspeicheroptionen der Ausgabe. |
| author | String | Initialen des Autors, die für Überarbeitungen verwendet werden sollen. |
| dateTime | DateTime | Das für Revisionen zu verwendende Datum und die Uhrzeit. |
| compareOptions | CompareOptions | Optionen zum Dokumentenvergleich. |

## Beispiele

Zeigt, wie man Dokumente vergleicht und die Ergebnisse als Bilder speichert.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente zu vergleichen:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
