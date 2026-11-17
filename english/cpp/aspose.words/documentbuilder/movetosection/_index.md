---
title: Aspose::Words::DocumentBuilder::MoveToSection method
linktitle: MoveToSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::MoveToSection method. Moves the cursor to the beginning of the body in a specified section in C++.'
type: docs
weight: 60000
url: /cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Moves the cursor to the beginning of the body in a specified section.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sectionIndex | int32_t | The index of the section to move to. |
## Remarks


When *sectionIndex* is greater than or equal to 0, it specifies an index from the beginning of the document with 0 being the first section. When *sectionIndex* is less than 0, it specified an index from the end of the document with -1 being the last section.

The cursor is moved to the first paragraph in the [Body](../../body/) of the specified section.

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
