---
title: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked metodu"
linktitle: "get_AspectRatioLocked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked metodu. Shape''s en-boy oranının C++'da kilitli olup olmadığını belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing/shapebase/get_aspectratiolocked/
---
## ShapeBase::get_AspectRatioLocked method


Şeklin en‑boy oranının kilitli olup olmadığını belirtir.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked()
```

## Açıklamalar


Varsayılan değer, [ShapeType](../../shapetype/) öğesine bağlıdır; [Image](../../shapetype/) için **true**, diğer şekil türleri için ise **false**'dır.

Yalnızca üst düzey şekiller için etkilidir.

## Örnekler



Bir şeklin en‑boy oranını kilitleme/açma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir şekil ekleyin. Bu belgeyi Microsoft Word'de açarsak, şekle sol tıklayarak ortaya çıkarmak için
// çevresinde sekiz boyutlandırma tutamacı bulunur; bunlara tıklayıp sürükleyerek boyutunu değiştirebiliriz.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Set the "AspectRatioLocked" property to "true" to preserve the shape's aspect ratio
// dört diyagonal boyutlandırma tutamacından herhangi birini kullandığınızda, bu tutamacılar görüntünün yüksekliğini ve genişliğini birlikte değiştirir.
// Yüksekliği ya da genişliği değiştiren herhangi bir ortogonal boyutlandırma tutamacı kullanmak yine de en‑boy oranını değiştirecektir.
// Set the "AspectRatioLocked" property to "false" to allow us to
// tüm boyutlandırma tutamacılarını kullanarak görüntünün en‑boy oranını serbestçe değiştirebilmemizi sağlar.
shape->set_AspectRatioLocked(lockAspectRatio);

doc->Save(get_ArtifactsDir() + u"Shape.AspectRatio.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
