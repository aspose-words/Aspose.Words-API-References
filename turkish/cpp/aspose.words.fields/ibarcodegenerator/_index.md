---
title: "Aspose::Words::Fields::IBarcodeGenerator interface"
linktitle: "IBarcodeGenerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::IBarcodeGenerator arayüzü. Barkod özel üreticisi için genel arayüz. Uygulama C++'da kullanıcı tarafından sağlanmalıdır."
type: docs
weight: 118000
url: /tr/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Barkod özel üreticisi için genel arayüz. Uygulama kullanıcı tarafından sağlanmalıdır.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Parametre kümesini kullanarak barkod görüntüsü oluştur (DisplayBarcode alanı için). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Parametre kümesini kullanarak barkod görüntüsü oluştur (eski tip Barcode alanı için). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
