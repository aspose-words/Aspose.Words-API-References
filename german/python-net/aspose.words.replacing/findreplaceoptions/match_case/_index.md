---
title: FindReplaceOptions.match_case property
linktitle: match_case property
articleTitle: match_case property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.match_case property. True indicates case-sensitive comparison, false indicates case-insensitive comparison."
type: docs
weight: 150
url: /de/python-net/aspose.words.replacing/findreplaceoptions/match_case/
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
# Wir können ein "FindReplaceOptions" Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
options = aw.replacing.FindReplaceOptions()
# Setzen Sie das "MatchCase"-Flag auf "true", um bei der Suche nach zu ersetzenden Zeichenketten die Groß‑ und Kleinschreibung zu berücksichtigen.
# Setzen Sie das "MatchCase"-Flag auf "false", um bei der Suche nach zu ersetzendem Text die Groß‑ und Kleinschreibung zu ignorieren.
options.match_case = match_case
doc.range.replace(pattern='Ruby', replacement='Jade', options=options)
self.assertEqual('Jade bought a ruby necklace.' if match_case else 'Jade bought a Jade necklace.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

