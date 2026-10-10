---
title: FindReplaceOptions.use_substitutions property
linktitle: use_substitutions property
articleTitle: use_substitutions property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.use_substitutions property. Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns"
type: docs
weight: 200
url: /zh/python-net/aspose.words.replacing/findreplaceoptions/use_substitutions/
---

## FindReplaceOptions.use_substitutions property

Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns.
The default value is ``False``.



```python
@property
def use_substitutions(self) -> bool:
    ...

@use_substitutions.setter
def use_substitutions(self, value: bool):
    ...

```

### Remarks

For the details on substitution elements please refer to:
https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.


### Examples

Shows how to recognize and use substitutions within replacement patterns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Jason gave money to Paul.')
regex = '([A-z]+) gave money to ([A-z]+)'
options = aw.replacing.FindReplaceOptions()
options.use_substitutions = True
# 使用旧版模式不支持许多高级功能，因此我们需要将其设置为 'false'。
options.legacy_mode = False
doc.range.replace_regex(pattern=regex, replacement='$2 took money from $1', options=options)
self.assertEqual(doc.get_text(), 'Paul took money from Jason.\x0c')
```

Shows how to replace the text with substitutions.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('John sold a car to Paul.')
builder.writeln('Jane sold a house to Joe.')
# 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
options = aw.replacing.FindReplaceOptions()
# 将 "UseSubstitutions" 属性设置为 "true" 以获取
# 查找和替换操作以识别替代元素。
# 将 "UseSubstitutions" 属性设置为 "false" 以忽略替代元素。
options.use_substitutions = use_substitutions
regex = '([A-z]+) sold a ([A-z]+) to ([A-z]+)'
doc.range.replace_regex(pattern=regex, replacement='$3 bought a $2 from $1', options=options)
self.assertEqual('Paul bought a car from John.\rJoe bought a house from Jane.' if use_substitutions else '$3 bought a $2 from $1.\r$3 bought a $2 from $1.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

