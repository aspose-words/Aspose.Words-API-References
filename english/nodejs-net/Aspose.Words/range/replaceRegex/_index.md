---
title: Range.replaceRegex method
linktitle: replaceRegex method
articleTitle: replaceRegex method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Range.replaceRegex method"
type: docs
weight: 100
url: /nodejs-net/Aspose.Words/range/replaceRegex/
---

## replaceRegex(pattern, replacement) {#string_string}

Replaces all occurrences of a character pattern specified by a regular expression with another string.


```js
replaceRegex(pattern: stringreplacement: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | string | A regular expression pattern used to find matches. |
| replacement | string | A string to replace all occurrences of pattern. |

### Remarks

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  

Use method[Range.replaceRegex()](./#string_string_findreplaceoptions) to have more flexible customization.



### Returns

The number of replacements made.


## replaceRegex(pattern, replacement, options) {#string_string_findreplaceoptions}

Replaces all occurrences of a character pattern specified by a regular expression with another string.


```js
replaceRegex(pattern: stringreplacement: stringoptions: Aspose.Words.Replacing.FindReplaceOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | string | A regular expression pattern used to find matches. |
| replacement | string | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../Aspose.Words.Replacing/findreplaceoptions/) | [FindReplaceOptions](../../../Aspose.Words.Replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  
* **&&** - & character
  



### Returns

The number of replacements made.


## See Also

* module [Aspose.Words](../../)
* class [Range](../)

