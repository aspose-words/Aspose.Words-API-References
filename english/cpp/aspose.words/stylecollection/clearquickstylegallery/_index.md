---
title: ClearQuickStyleGallery
second_title: Aspose.Words for C++ API Reference
description: Removes all styles from the Quick Style Gallery panel.
type: docs
weight: 27
url: /cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method


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

