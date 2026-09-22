---
title: "Aspose::Words::Fields::IFieldResultFormatter arayüz"
linktitle: "IFieldResultFormatter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::IFieldResultFormatter arayüz. Bu arayüzü, alan sonucunun C++'da nasıl biçimlendirileceğini kontrol etmek istiyorsanız uygulayın."
type: docs
weight: 121000
url: /tr/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Alan sonucunun nasıl biçimlendirileceğini kontrol etmek istiyorsanız bu arayüzü uygulayın.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Aspose.Words bir büyük harf biçim anahtarını uyguladığında çağrılır, ör. \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Aspose.Words bir sayı biçim anahtarını uyguladığında çağrılır, ör. \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Aspose.Words bir tarih/saat biçim anahtarını uyguladığında çağrılır, ör. \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Aspose.Words bir sayısal biçim anahtarını uyguladığında çağrılır, ör. \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
