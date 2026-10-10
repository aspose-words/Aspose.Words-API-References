---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor yöntemi"
linktitle: "get_InsertCellColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertCellColor yöntemi. Eklenen hücreler için kullanılacak rengi belirtmeye izin verir Insertion. Varsayılan değer C++'da Mavi'dir."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Eklenen hücreler için kullanılacak rengi belirtmeye izin verir [Insertion](../../../aspose.words/revisiontype/). Varsayılan değer [Mavi](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Örnekler



Ekleme/silme hücresi revizyon rengiyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## Ayrıca Bakınız

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
