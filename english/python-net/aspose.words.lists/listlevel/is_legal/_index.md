---
title: ListLevel.is_legal property
linktitle: is_legal property
articleTitle: is_legal property
second_title: Aspose.Words for Python
description: "ListLevel.is_legal property. True if the level turns all inherited numbers to Arabic, false if it preserves their number style."
type: docs
weight: 50
url: /python-net/aspose.words.lists/listlevel/is_legal/
---

## ListLevel.is_legal property

True if the level turns all inherited numbers to Arabic, false if it preserves their number style.


```python
@property
def is_legal(self) -> bool:
    ...

@is_legal.setter
def is_legal(self, value: bool):
    ...

```

### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)

# Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
# These will look like "Appendix A", "Appendix B"...
list.list_levels[0].number_format = "Appendix \u0000"
list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
list.list_levels[0].linked_style = doc.styles.get_by_name("Heading 1")

# Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
# If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
list.list_levels[1].number_format = "Section (\u0000.\u0001)"
list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO

# Note that the higher-level uses UppercaseLetter numbering.
# We can set the "is_legal" property to use Arabic numbers for the higher list levels.
list.list_levels[1].is_legal = True
list.list_levels[1].restart_after_level = 0

# Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
# These list labels will look like "-I-", "-II-"...
list.list_levels[2].number_format = "-\u0002-"
list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
list.list_levels[2].restart_after_level = 1

# Make labels of all list levels bold.
for level in list.list_levels:
    level.font.bold = True

# Apply list formatting to the current paragraph.
builder.list_format.list = list

# Create list items that will display all three of our list levels.
for n in range(2):
    for i in range(3):
        builder.list_format.list_level_number = i
        builder.writeln(f"Level {i}")

builder.list_format.remove_numbers()

doc.save(ARTIFACTS_DIR + "Lists.create_list_restart_after_higher.docx")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

