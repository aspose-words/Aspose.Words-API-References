---
title: Aspose::Words::StyleCollection::ClearQuickStyleGallery method
linktitle: ClearQuickStyleGallery
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::StyleCollection::ClearQuickStyleGallery method. Removes all styles from the Quick Style Gallery panel in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Removes all styles from the Quick [Style](../../style/) Gallery panel.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Examples



Shows how to remove styles from [Style](../../style/) Gallery panel. 
```cpp
auto doc = MakeObject<Document>();

// Note that remove styles work only with DOCX format for now.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(ArtifactsDir + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## See Also

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
