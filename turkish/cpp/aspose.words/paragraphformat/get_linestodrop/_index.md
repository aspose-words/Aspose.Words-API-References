---
title: "Aspose::Words::ParagraphFormat::get_LinesToDrop method"
linktitle: "get_LinesToDrop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_LinesToDrop method. C++'ta damla başlık yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını alır veya ayarlar."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/paragraphformat/get_linestodrop/
---
## ParagraphFormat::get_LinesToDrop method


Büyük harf yüksekliğini hesaplamak için kullanılan paragraf metni satır sayısını alır veya ayarlar.

```cpp
int32_t Aspose::Words::ParagraphFormat::get_LinesToDrop()
```


## Örnekler



Bir damla başlığın boyutunu nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Değiştirin "LinesToDrop" özelliğini bir paragrafı damla baş harf olarak atamak için,
// bu, onu bir sonraki paragrafı süsleyecek büyük bir büyük harfe dönüştürecektir.
// Bu özelliğe 4 değerini vererek damla baş harfe dört metin satırı yüksekliği verin.
builder->get_ParagraphFormat()->set_LinesToDrop(4);
builder->Writeln(u"H");

// "LinesToDrop" özelliğini 0'a sıfırlayarak bir sonraki paragrafı sıradan bir paragraf haline getirin.
// Bu paragraftaki metin damla baş harfin etrafına dolanacaktır.
builder->get_ParagraphFormat()->set_LinesToDrop(0);
builder->Writeln(u"ello world!");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LinesToDrop.odt");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
