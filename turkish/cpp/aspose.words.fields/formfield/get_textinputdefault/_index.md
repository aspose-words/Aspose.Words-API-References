---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault metodu"
linktitle: "get_TextInputDefault"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault metodu. C++'de bir metin form alanının varsayılan dizesini veya bir hesaplama ifadesini alır veya ayarlar."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Metin form alanının varsayılan dizesini veya bir hesaplama ifadesini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Açıklamalar


Bu özelliğin anlamı, [TextInputType](../get_textinputtype/) özelliğinin değerine bağlıdır.

Eğer [TextInputType](../get_textinputtype/) [Regular](../../textformfieldtype/) veya [Number](../../textformfieldtype/) ise, bu dize metin form alanı için varsayılan dizeyi belirtir. Bu dize, form alanı boş olduğunda Microsoft Word'ün belgede göstereceği içeriktir.

Eğer [TextInputType](../get_textinputtype/) [Calculated](../../textformfieldtype/) ise, bu dize hesaplanacak ifadeyi tutar. İfade, Microsoft Word formül alanı gereksinimlerine göre geçerli bir formül olmalıdır. Bu özelliği kullanarak yeni bir ifade ayarladığınızda, Aspose.Words formül sonucunu otomatik olarak hesaplar ve form alanına ekler.

Microsoft Word en fazla 255 karakter uzunluğunda dizelere izin verir.
## Ayrıca Bakınız

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
