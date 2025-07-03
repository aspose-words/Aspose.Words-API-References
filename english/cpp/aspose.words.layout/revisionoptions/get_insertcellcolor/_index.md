---
title: Aspose::Words::Layout::RevisionOptions::get_InsertCellColor method
linktitle: get_InsertCellColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::RevisionOptions::get_InsertCellColor method. Allows to specify the color to be used for inserted cells Insertion. Default value is Blue in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Allows to specify the color to be used for inserted cells [Insertion](../../../aspose.words/revisiontype/). Default value is [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Examples



Shows how to work with insert/delete cell revision color. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## See Also

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
