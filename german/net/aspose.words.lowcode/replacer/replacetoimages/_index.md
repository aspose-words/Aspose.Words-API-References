---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words für .NET
description: Transformieren Sie Ihre Eingabedateien mühelos, indem Sie Zeichenmuster durch benutzerdefinierte Zeichenfolgen ersetzen und mit unserer Methode „ReplaceToImages“ beeindruckende Bilder generieren.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument ersetzt und das Ergebnis in Bildern gespeichert werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument zu ersetzen:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

Ersetzt alle Vorkommen eines angegebenen Zeichenfolgenmusters durch eine Ersatzzeichenfolge in der Eingabedatei. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen. |
| pattern | String | Eine zu ersetzende Zeichenfolge. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument durch Dokumente aus dem Stream ersetzt und das Ergebnis in Bildern gespeichert werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch Dokumente aus dem Stream zu ersetzen:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

    FindReplaceOptions options = new FindReplaceOptions();
    options.FindWholeWordsOnly = false;
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Ersetzt alle Vorkommen eines angegebenen regulären Ausdrucksmusters durch eine Ersatzzeichenfolge in der Eingabedatei. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | String | Der Name der Eingabedatei. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument durch reguläre Ausdrücke ersetzt und das Ergebnis in Bildern gespeichert werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument durch reguläre Ausdrücke zu ersetzen:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Ersetzt alle Vorkommen eines angegebenen regulären Ausdrucksmusters durch eine Ersatzzeichenfolge in der Eingabedatei. Rendert die Ausgabe in Bilder.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | Stream | Der Eingabedateistream. |
| saveOptions | ImageSaveOptions | Die Speicheroptionen. |
| pattern | Regex | Ein reguläres Ausdrucksmuster zum Suchen von Übereinstimmungen. |
| replacement | String | Eine Zeichenfolge zum Ersetzen aller Vorkommen des Musters. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) Objekt, um zusätzliche Optionen anzugeben. |

## Beispiele

Zeigt, wie Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream durch reguläre Ausdrücke ersetzt und das Ergebnis in Bildern gespeichert werden.

```csharp
// Es gibt mehrere Möglichkeiten, Zeichenfolgen im Dokument mithilfe von Dokumenten aus dem Stream durch reguläre Ausdrücke zu ersetzen:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
