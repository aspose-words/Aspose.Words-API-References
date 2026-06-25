---
title: Aspose::Words::Document::RemoveCustomizations method
linktitle: RemoveCustomizations
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::RemoveCustomizations method. Removes toolbar and keyboard command customizations from the document in C++.'
type: docs
weight: 67750
url: /cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Removes toolbar and keyboard command customizations from the document.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Examples



Shows how to remove toolbar and keyboard command customizations from the document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Remove all custom document UI customizations, including custom context menu entries.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
