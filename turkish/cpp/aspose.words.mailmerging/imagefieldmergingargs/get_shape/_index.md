---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape metodu"
linktitle: "get_Shape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape yöntemi. C++'ta posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Açıklamalar


Bu özellik belirtildiğinde, posta birleştirme motoru [ImageFileName](../get_imagefilename/) veya [ImageStream](../get_imagestream/) gibi diğer tüm özellikleri yok sayar ve sadece şekli belgeye ekler.

Bu özelliği bir görüntü birleştirme alanını birleştirme sürecini tam olarak kontrol etmek için kullanın. Örneğin, sonuç düğümünü ince ayarlamak için [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) veya başka bir şekil özelliği belirtebilirsiniz. Ancak, şeklin içeriğini sağlamaktan sizin sorumlu olduğunuzu lütfen unutmayın.
## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
