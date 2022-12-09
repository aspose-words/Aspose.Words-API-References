---
title: get_SpaceBeforeAuto
second_title: Aspose.Words for C++ API Reference
description: True if the amount of spacing before the paragraph is set automatically.
type: docs
weight: 430
url: /cpp/aspose.words/paragraphformat/get_spacebeforeauto/
---
## ParagraphFormat::get_SpaceBeforeAuto method


True if the amount of spacing before the paragraph is set automatically.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto()
```

## Remarks


When set to **true**, overrides the effect of [SpaceBefore](../get_spacebefore/).

When you set paragraph Space Before and Space After to Auto, **Microsoft** Word adds 14 points spacing between paragraphs automatically according to the following rules:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



## Examples



Shows how to set automatic paragraph spacing. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Apply a large amount of spacing before and after paragraphs that this builder will create.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Set these flags to "true" to apply automatic spacing,
// effectively ignoring the spacing in the properties we set above.
// Leave them as "false" will apply our custom paragraph spacing.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Insert two paragraphs that will have spacing above and below them and save the document.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(ArtifactsDir + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
