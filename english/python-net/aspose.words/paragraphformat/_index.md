---
title: ParagraphFormat class
linktitle: ParagraphFormat class
articleTitle: ParagraphFormat class
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphFormat class. Represents all the formatting for a paragraph"
type: docs
weight: 900
url: /python-net/aspose.words/paragraphformat/
---

## ParagraphFormat class

Represents all the formatting for a paragraph.
To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/python-net/working-with-paragraphs/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [add_space_between_far_east_and_alpha](./add_space_between_far_east_and_alpha/) | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph. |
| [add_space_between_far_east_and_digit](./add_space_between_far_east_and_digit/) | Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of numbers and regions of East Asian text in the current paragraph. |
| [alignment](./alignment/) | Gets or sets text alignment for the paragraph. |
| [baseline_alignment](./baseline_alignment/) | Gets or sets fonts vertical position on a line. |
| [bidi](./bidi/) | Gets or sets whether this is a right-to-left paragraph. |
| [borders](./borders/) | Gets collection of borders of the paragraph. |
| [character_unit_first_line_indent](./character_unit_first_line_indent/) | Gets or sets the value (in characters) for the first-line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [character_unit_left_indent](./character_unit_left_indent/) | Gets or sets the left indent value (in characters) for the specified paragraphs. |
| [character_unit_right_indent](./character_unit_right_indent/) | Gets or sets the right indent value (in characters) for the specified paragraphs. |
| [drop_cap_position](./drop_cap_position/) | Gets or sets the position for a drop cap text. |
| [far_east_line_break_control](./far_east_line_break_control/) | Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph. |
| [first_line_indent](./first_line_indent/) | Gets or sets the value (in points) for a first line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent. |
| [hanging_punctuation](./hanging_punctuation/) | Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph. |
| [is_heading](./is_heading/) | True when the paragraph style is one of the built-in Heading styles. |
| [is_list_item](./is_list_item/) | True when the paragraph is an item in a bulleted or numbered list. |
| [keep_together](./keep_together/) | True if all lines in the paragraph are to remain on the same page. |
| [keep_with_next](./keep_with_next/) | True if the paragraph is to remains on the same page as the paragraph that follows it. |
| [left_indent](./left_indent/) | Gets or sets the value (in points) that represents the left indent for paragraph. |
| [line_spacing](./line_spacing/) | Gets or sets the line spacing (in points) for the paragraph. |
| [line_spacing_rule](./line_spacing_rule/) | Gets or sets the line spacing for the paragraph. |
| [line_unit_after](./line_unit_after/) | Gets or sets the amount of spacing (in gridlines) after the paragraphs. |
| [line_unit_before](./line_unit_before/) | Gets or sets the amount of spacing (in gridlines) before the paragraphs. |
| [lines_to_drop](./lines_to_drop/) | Gets or sets the number of lines of the paragraph text used to calculate the drop cap height. |
| [no_space_between_paragraphs_of_same_style](./no_space_between_paragraphs_of_same_style/) | When ``True``, [ParagraphFormat.space_before](./space_before/) and [ParagraphFormat.space_after](./space_after/) will be ignored between the paragraphs of the same style. |
| [outline_level](./outline_level/) | Specifies the outline level of the paragraph in the document. |
| [page_break_before](./page_break_before/) | True if a page break is forced before the paragraph. |
| [right_indent](./right_indent/) | Gets or sets the value (in points) that represents the right indent for paragraph. |
| [shading](./shading/) | Returns a [Shading](../shading/) object that refers to the shading formatting for the paragraph. |
| [snap_to_grid](./snap_to_grid/) | Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph. |
| [space_after](./space_after/) | Gets or sets the amount of spacing (in points) after the paragraph. |
| [space_after_auto](./space_after_auto/) | True if the amount of spacing after the paragraph is set automatically. |
| [space_before](./space_before/) | Gets or sets the amount of spacing (in points) before the paragraph. |
| [space_before_auto](./space_before_auto/) | True if the amount of spacing before the paragraph is set automatically. |
| [style](./style/) | Gets or sets the paragraph style applied to this formatting. |
| [style_identifier](./style_identifier/) | Gets or sets the locale independent style identifier of the paragraph style applied to this formatting. |
| [style_name](./style_name/) | Gets or sets the name of the paragraph style applied to this formatting. |
| [suppress_auto_hyphens](./suppress_auto_hyphens/) | Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings. |
| [suppress_line_numbers](./suppress_line_numbers/) | Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section. |
| [tab_stops](./tab_stops/) | Gets the collection of custom tab stops defined for this object. |
| [widow_control](./widow_control/) | True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph. |
| [word_wrap](./word_wrap/) | If this property is ``False``, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets to default paragraph formatting. |

### Examples

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()

# A blank document contains one section, one body and one paragraph.
# Call the "remove_all_children" method to remove all those nodes,
# and end up with a document node with no children.
doc.remove_all_children()

# This document now has no composite child nodes that we can add content to.
# If we wish to edit it, we will need to repopulate its node collection.
# First, create a new section, and then append it as a child to the root document node.
section = aw.Section(doc)
doc.append_child(section)

# Set some page setup properties for the section.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER

# A section needs a body, which will contain and display all its contents
# on the page between the section's header and footer.
body = aw.Body(doc)
section.append_child(body)

# Create a paragraph, set some formatting properties, and then append it as a child to the body.
para = aw.Paragraph(doc)

para.paragraph_format.style_name = "Heading 1"
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER

body.append_child(para)

# Finally, add some content to do the document. Create a run,
# set its appearance and contents, and then append it as a child to the paragraph.
run = aw.Run(doc)
run.text = "Hello World!"
run.font.color = drawing.Color.red
para.append_child(run)

self.assertEqual("Hello World!", doc.get_text().strip())

doc.save(ARTIFACTS_DIR + "Section.create_manually.docx")
```

### See Also

* module [aspose.words](../)

