---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words per .NET
description: Trasforma senza sforzo i tuoi file di input sostituendo i modelli di caratteri con stringhe personalizzate e generando immagini straordinarie con il nostro metodo ReplaceToImages.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa sostitutiva nel file di input. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| pattern | String | Una stringa da sostituire. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) oggetto per specificare opzioni aggiuntive. |

## Esempi

Mostra come sostituire una stringa nel documento e salvare il risultato nelle immagini.

```csharp
// Esistono diversi modi per sostituire una stringa nel documento:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

Sostituisce tutte le occorrenze di un modello di stringa di caratteri specificato con una stringa sostitutiva nel file di input. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| pattern | String | Una stringa da sostituire. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) oggetto per specificare opzioni aggiuntive. |

## Esempi

Mostra come sostituire una stringa nel documento utilizzando i documenti dal flusso e salvare il risultato nelle immagini.

```csharp
// Esistono diversi modi per sostituire una stringa nel documento utilizzando i documenti dal flusso:
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

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Sostituisce tutte le occorrenze di un modello di espressione regolare specificato con una stringa di sostituzione nel file di input. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| pattern | Regex | Un modello di espressione regolare utilizzato per trovare corrispondenze. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) oggetto per specificare opzioni aggiuntive. |

## Esempi

Mostra come sostituire una stringa con un'espressione regolare nel documento e salvare il risultato nelle immagini.

```csharp
// Esistono diversi modi per sostituire una stringa con un'espressione regolare nel documento:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Sostituisce tutte le occorrenze di un modello di espressione regolare specificato con una stringa di sostituzione nel file di input. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| pattern | Regex | Un modello di espressione regolare utilizzato per trovare corrispondenze. |
| replacement | String | Una stringa per sostituire tutte le occorrenze di pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) oggetto per specificare opzioni aggiuntive. |

## Esempi

Mostra come sostituire una stringa con un'espressione regolare nel documento utilizzando i documenti dal flusso e salvare il risultato nelle immagini.

```csharp
// Esistono diversi modi per sostituire una stringa con un'espressione regolare nel documento utilizzando i documenti dal flusso:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
