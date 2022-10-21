---
title: FontConfigSubstitutionRule
second_title: Aspose.Words for Java API Reference
description: Font config substitution rule.
type: docs
weight: 276
url: /java/com.aspose.words/fontconfigsubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule)
```
public class FontConfigSubstitutionRule extends FontSubstitutionRule
```

Font config substitution rule.

To learn more, visit the **Working with Fonts** documentation article.

This rule uses fontconfig utility on Linux (and other Unix-like) platforms to get the substitution if the original font is not available.

If fontconfig utility is not available then this rule will be ignored.
## Methods

| Method | Description |
| --- | --- |
| [setEnabled(boolean value)](#setEnabled-boolean-) | Specifies whether the rule is enabled or not. |
| [isFontConfigAvailable()](#isFontConfigAvailable--) | Check if fontconfig utility is available or not. |
| [resetCache()](#resetCache--) | Resets the cache of fontconfig calling results. |
### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


Specifies whether the rule is enabled or not.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isFontConfigAvailable() {#isFontConfigAvailable--}
```
public boolean isFontConfigAvailable()
```


Check if fontconfig utility is available or not.

**Returns:**
boolean
### resetCache() {#resetCache--}
```
public void resetCache()
```


Resets the cache of fontconfig calling results.

