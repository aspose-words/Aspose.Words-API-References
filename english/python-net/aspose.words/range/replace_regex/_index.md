---
title: replace_regex method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.Range.replace_regex method"
type: docs
weight: 100
url: /python-net/aspose.words/range/replace_regex/
---

## replace_regex(pattern, replacement) {#str_str}

Replaces all occurrences of a character pattern specified by a regular expression with another string.


```python
def replace_regex(self, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | str |  |
| replacement | str |  |

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  

Use method[Range.replace_regex()](./#str_str_findreplaceoptions) to have more flexible customization.



### Returns

The number of replacements made.


## replace_regex(pattern, replacement, options) {#str_str_findreplaceoptions}

Replaces all occurrences of a character pattern specified by a regular expression with another string.


```python
def replace_regex(self, pattern: str, replacement: str, options: aspose.words.replacing.FindReplaceOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | str |  |
| replacement | str |  |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) |  |

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

* module [aspose.words](../../)
* class [Range](../)

