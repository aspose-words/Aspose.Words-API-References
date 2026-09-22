---
title: "Aspose::Words::Document::RemoveCustomizations method"
linktitle: "RemoveCustomizations"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::RemoveCustomizations yöntemi. C++'da belgeden araç çubuğu ve klavye komutu özelleştirmelerini kaldırır."
type: docs
weight: 67750
url: /tr/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Belgeden araç çubuğu ve klavye komut özelleştirmelerini kaldırır.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Örnekler



Araç çubuğu ve klavye komutu özelleştirmelerinin belgeden nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Özel bağlam menüsü girişleri dahil, tüm özel belge UI özelleştirmelerini kaldır.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
