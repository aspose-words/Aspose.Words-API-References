---
title: Replace
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 80
url: /net/aspose.words/range/replace/
---
## Range.Replace method (1 of 4)

Replaces all occurrences of a specified character string pattern with a replacement string.

```csharp
public int Replace(string pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |

## Return Value

The number of replacements made.

### Remarks

The pattern will not be used as regular expression. Please use [`Replace`](../replace) if you need regular expressions.

Used case-insensitive comparison.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break

Use method [`Replace`](../replace) to have more flexible customization.

### Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserts paragraph break after Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

### See Also

* class [Range](../../range)
* namespace [Aspose.Words](../../range)
* assembly [Aspose.Words](../../../)

---

## Range.Replace method (2 of 4)

Replaces all occurrences of a character pattern specified by a regular expression with another string.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |

## Return Value

The number of replacements made.

### Remarks

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break

Use method [`Replace`](../replace) to have more flexible customization.

### Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Replaces each number with paragraph break.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

### See Also

* class [Range](../../range)
* namespace [Aspose.Words](../../range)
* assembly [Aspose.Words](../../../)

---

## Range.Replace method (3 of 4)

Replaces all occurrences of a specified character string pattern with a replacement string.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | String | A string to be replaced. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions) object to specify additional options. |

## Return Value

The number of replacements made.

### Remarks

The pattern will not be used as regular expression. Please use [`Replace`](../replace) if you need regular expressions.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break
* **&amp;&amp;** - &amp; character

### Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Inserts paragraph break after Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

### See Also

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* namespace [Aspose.Words](../../range)
* assembly [Aspose.Words](../../../)

---

## Range.Replace method (4 of 4)

Replaces all occurrences of a character pattern specified by a regular expression with another string.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | Regex | A regular expression pattern used to find matches. |
| replacement | String | A string to replace all occurrences of pattern. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions) object to specify additional options. |

## Return Value

The number of replacements made.

### Remarks

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **&amp;p** - paragraph break
* **&amp;b** - section break
* **&amp;m** - page break
* **&amp;l** - manual line break
* **&amp;&amp;** - &amp; character

### Examples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Replaces each number with paragraph break.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

### See Also

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* namespace [Aspose.Words](../../range)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
