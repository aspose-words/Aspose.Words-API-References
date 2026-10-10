---
title: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor yöntemi"
linktitle: "get_DeleteCellColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor yöntemi. Silinen hücreler için kullanılacak rengi belirtmenizi sağlar Deletion. Varsayılan değer C++'da Pink'tir."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Silinen hücreler için kullanılacak rengi belirtmenizi sağlar [Deletion](../../../aspose.words/revisiontype/). Varsayılan değer [Pink](../../revisioncolor/)dir.

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
