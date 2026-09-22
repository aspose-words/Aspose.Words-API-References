---
title: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer yöntemi"
linktitle: "get_UseGdiEmfRenderer"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer yöntemi. C++'ta EMF olarak kaydederken GDI+ veya Aspose.Words metafile işleyicisinin kullanılacağını belirleyen bir değeri alır veya ayarlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


EMF olarak kaydederken GDI+ veya Aspose.Words metafile renderleyicisinin kullanılacağını belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Açıklamalar


Eğer **true** olarak ayarlanırsa GDI+ metafile işleyicisi kullanılır. Yani içerik GDI+ grafik nesnesine yazılır ve metafile olarak kaydedilir.

Eğer **false** olarak ayarlanırsa Aspose.Words metafile işleyicisi kullanılır. Yani içerik doğrudan Aspose.Words ile metafile formatına yazılır.

Yalnızca EMF olarak kaydederken etkili olur.

GDI+ kaydetme yalnızca .NET üzerinde çalışır.

Varsayılan değer **true**'dır.

## Örnekler



Bir belge .emf'ye dönüştürülürken işleyicinin nasıl seçileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Belgeyi bir EMF görüntüsü olarak kaydettiğimizde, görüntü için bir işleyici seçmek amacıyla bir SaveOptions nesnesi geçirebiliriz.
// If we set the "UseGdiEmfRenderer" flag to "true", Aspose.Words will use the GDI+ renderer.
// Eğer "UseGdiEmfRenderer" bayrağını "false" olarak ayarlarsak, Aspose.Words kendi metafile renderleyicisini kullanacaktır.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## Ayrıca Bakınız

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
