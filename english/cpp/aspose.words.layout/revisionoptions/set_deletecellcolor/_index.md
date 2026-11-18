---
title: Aspose::Words::Layout::RevisionOptions::set_DeleteCellColor method
linktitle: set_DeleteCellColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionOptions::set_DeleteCellColor method. Allows to specify the color to be used for deleted cells Deletion. Default value is Pink in C++.'
type: docs
weight: 23500
url: /cpp/aspose.words.layout/revisionoptions/set_deletecellcolor/
---
## RevisionOptions::set_DeleteCellColor method


Allows to specify the color to be used for deleted cells [Deletion](../../../aspose.words/revisiontype/). Default value is [Pink](../../revisioncolor/).

```cpp
void Aspose::Words::Layout::RevisionOptions::set_DeleteCellColor(Aspose::Words::Layout::RevisionColor value)
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
