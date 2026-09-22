---
title: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles yöntemi"
linktitle: "get_AlwaysCompressMetafiles"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles yöntemi. false olduğunda, performans nedeniyle küçük metafile'lar sıkıştırılmaz. Varsayılan değer true'tır, tüm metafile'lar boyutu ne olursa olsun C++ içinde sıkıştırılır."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/docsaveoptions/get_alwayscompressmetafiles/
---
## DocSaveOptions::get_AlwaysCompressMetafiles method


**false** olduğunda, küçük metafile'lar performans nedeni ile sıkıştırılmaz. Varsayılan değer **true**'dur; tüm metafile'lar boyutu ne olursa olsun sıkıştırılır.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_AlwaysCompressMetafiles() const
```


## Örnekler



Bir belgeyi kaydederken metafile sıkıştırmasının nasıl değiştirileceğini gösterir.
```cpp
// Microsoft Equation 3.0 formülü içeren bir belgeyi açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Microsoft equation object.docx");

// Bir belgeyi kaydettiğimizde, daha küçük metafile'lar performans nedenleriyle sıkıştırılmaz.
// Kaydederken her metafile'ı sıkıştırmak için SaveOptions nesnesinde bir bayrak ayarlayabiliriz.
// LibreOffice gibi bazı editörler sıkıştırılmamış metafile'ları okuyamaz.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_AlwaysCompressMetafiles(compressAllMetafiles);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.AlwaysCompressMetafiles.docx", saveOptions);
```

## Ayrıca Bakınız

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
