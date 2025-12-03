---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words for .NET
description: Effortlessly transform your input files by replacing character patterns with custom strings and generating stunning images with our ReplaceToImages method.
type: docs
weight: 30
url: /net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string*) {#replacetoimages_4}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_5}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

## Examples

Shows how to replace string in the document and save result to images.

```csharp
// There is a several ways to replace string in the document:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string*) {#replacetoimages}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

## Examples

Shows how to replace string in the document using documents from the stream and save result to images.

```csharp
// There is a several ways to replace string in the document using documents from the stream:
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

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_7}

Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

## Examples

Shows how to replace string with regex in the document and save result to images.

```csharp
// There is a several ways to replace string with regex in the document:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string*) {#replacetoimages_6}

Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

## Examples

Shows how to replace string with regex in the document using documents from the stream and save result to images.

```csharp
// There is a several ways to replace string with regex in the document using documents from the stream:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string*) {#replacetoimages_2}

Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| saveOptions | ImageSaveOptions | The save options. |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |

### See Also

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Replacer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
