---
title: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape yöntemi"
linktitle: "get_CurrentShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape yöntemi. C++'ta kaydedilmek üzere olan şekil veya grup şekline karşılık gelen ShapeBase nesnesini alır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Kaydedilmek üzere olan şekil veya grup şekline karşılık gelen [ShapeBase](../../../aspose.words.drawing/shapebase/) nesnesini alır.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Açıklamalar


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words, belgede bulunan her resim için benzersiz bir dosya adı oluşturmak amacıyla belge dosya adını ve benzersiz bir sayıyı kullanır. [CurrentShape](./) özelliğini, şekil özelliklerini (örneğin [Title](../../../aspose.words.drawing/imagedata/get_title/) (yalnızca Şekil), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (yalnızca Şekil) ve [Name](../../../aspose.words.drawing/shapebase/get_name/)) inceleyerek "daha iyi" bir dosya adı oluşturmak için kullanabilirsiniz. Elbette başka özellikler veya kriterler kullanarak da dosya adları oluşturabilirsiniz, ancak alt dosya adlarının dışa aktarma işlemi içinde benzersiz olması gerektiğini unutmayın.

Belgedeki bazı resimler mevcut olmayabilir. Resim kullanılabilirliğini kontrol etmek için [IsImageAvailable](../get_isimageavailable/) özelliğini kullanın.
## Ayrıca Bakınız

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
