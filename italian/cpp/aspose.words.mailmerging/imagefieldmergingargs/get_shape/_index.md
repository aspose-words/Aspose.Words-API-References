---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape metodo"
linktitle: "get_Shape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape. Specifica la forma che il motore di stampa unione deve inserire nel documento in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Specifica la forma che il motore di stampa unione deve inserire nel documento.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Note


Quando questa proprietà è specificata, il motore di stampa unione ignora tutte le altre proprietà come [ImageFileName](../get_imagefilename/) o [ImageStream](../get_imagestream/) e inserisce semplicemente la forma nel documento.

Utilizza questa proprietà per controllare completamente il processo di unione di un campo immagine. Ad esempio, puoi specificare [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) o qualsiasi altra proprietà della forma per perfezionare il nodo risultante. Tuttavia, tieni presente che sei responsabile di fornire il contenuto della forma.
## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
