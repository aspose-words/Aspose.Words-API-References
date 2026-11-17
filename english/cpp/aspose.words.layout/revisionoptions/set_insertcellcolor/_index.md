---
title: Aspose::Words::Layout::RevisionOptions::set_InsertCellColor method
linktitle: set_InsertCellColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionOptions::set_InsertCellColor method. Allows to specify the color to be used for inserted cells Insertion. Default value is Blue in C++.'
type: docs
weight: 25500
url: /cpp/aspose.words.layout/revisionoptions/set_insertcellcolor/
---
## RevisionOptions::set_InsertCellColor method


Allows to specify the color to be used for inserted cells [Insertion](../../../aspose.words/revisiontype/). Default value is [Blue](../../revisioncolor/).

```cpp
void Aspose::Words::Layout::RevisionOptions::set_InsertCellColor(Aspose::Words::Layout::RevisionColor value)
```

## Examples


Shows how to work with insert/delete cell revision color.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Cell revisions.docx"));

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```
## See Also

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
