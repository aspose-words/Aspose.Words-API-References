---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
second_title: Aspose.Words for .NET API Reference
description: ImageFieldMergingArgs Shape property. Specifies the shape that the mail merge engine must insert into the document in C#.
type: docs
weight: 60
url: /net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Specifies the shape that the mail merge engine must insert into the document.

```csharp
public Shape Shape { get; set; }
```

## Remarks

When this property is specified, the mail merge engine ignores all other properties like [`ImageFileName`](../imagefilename/) or [`ImageStream`](../imagestream/) and simply inserts the shape into the document.

Use this property to fully control the process of merging an image merge field. For example, you can specify [`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/) or any other shape property to fine tune the resulting node. However, please note that you are responsible for providing the content of the shape.

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* namespace [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* assembly [Aspose.Words](../../../)
