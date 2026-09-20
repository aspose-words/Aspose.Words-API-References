---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape метод"
linktitle: "get_Shape"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape. Указывает форму, которую движок слияния почты должен вставить в документ в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Указывает форму, которую движок слияния почты должен вставить в документ.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Примечания


Когда это свойство указано, движок слияния почты игнорирует все остальные свойства, такие как [ImageFileName](../get_imagefilename/) или [ImageStream](../get_imagestream/), и просто вставляет форму в документ.

Используйте это свойство для полного контроля процесса слияния поля изображения. Например, вы можете указать [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) или любое другое свойство формы, чтобы точно настроить полученный узел. Однако обратите внимание, что вы отвечаете за предоставление содержимого формы.
## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
