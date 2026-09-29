---
title: FindReplaceOptions.match_case property
linktitle: match_case property
articleTitle: match_case property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.match_case property. True indicates case-sensitive comparison, false indicates case-insensitive comparison."
type: docs
weight: 150
url: /sv/python-net/aspose.words.replacing/findreplaceoptions/match_case/
---

## FindReplaceOptions.match_case property

True indicates case-sensitive comparison, false indicates case-insensitive comparison.


```python
@property
def match_case(self) -> bool:
    ...

@match_case.setter
def match_case(self, value: bool):
    ...

```

### Examples

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Ruby bought a ruby necklace.')
# Vi kan använda ett \"FindReplaceOptions\"-objekt för att ändra sök‑och‑ersätt‑processen.
options = aw.replacing.FindReplaceOptions()
# Ställ in flaggan \"MatchCase\" till \"true\" för att tillämpa skiftlägeskänslighet när du söker efter strängar att ersätta.
# Ställ in flaggan \"MatchCase\" till \"false\" för att ignorera skiftläge när du söker efter text att ersätta.
options.match_case = match_case
doc.range.replace(pattern='Ruby', replacement='Jade', options=options)
self.assertEqual('Jade bought a ruby necklace.' if match_case else 'Jade bought a Jade necklace.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

