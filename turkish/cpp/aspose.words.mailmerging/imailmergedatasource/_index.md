---
title: "Aspose::Words::MailMerging::IMailMergeDataSource arayüzü"
linktitle: "IMailMergeDataSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::IMailMergeDataSource arayüzü. Özel bir veri kaynağından, örneğin nesne listelerinden, posta birleştirmeye izin vermek için bu arayüzü uygulayın. Ana-çocuk veri de C++'ta desteklenir."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Nesne listesi gibi özel bir veri kaynağından posta birleştirmeye izin vermek için bu arayüzü uygulayın. Ana‑detay verileri de desteklenir.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Veri kaynağının adını döndürür. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Aspose.Words posta birleştirme motoru, iç içe bir posta birleştirme bölgesi başlangıcına rastladığında bu yöntemi çağırır. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Veri kaynağındaki bir sonraki kayda ilerler. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir veri kaynağı oluşturulduğunda, BOF (ilk kayıttan önce) konumuna işaret edecek şekilde başlatılmalıdır. Aspose.Words posta birleştirme motoru, bir sonraki kayda ilerlemek için [MoveNext](./movenext/) yöntemini ve ardından belgede veya mevcut posta birleştirme bölgesinde karşılaştığı her bir birleştirme alanı için [GetValue()](./getvalue/) yöntemini çağıracaktır.

## Ayrıca Bakınız

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
