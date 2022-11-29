---
title: get_Shape
second_title: Aspose.Words for C++ API Reference
description: Specifies the shape that the mail merge engine must insert into the document.
type: docs
weight: 66
url: /cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Specifies the shape that the mail merge engine must insert into the document.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Remarks


When this property is specified, the mail merge engine ignores all other properties like [ImageFileName](../get_imagefilename/) or [ImageStream](../get_imagestream/) and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape. 
## See Also

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words](../../../)
