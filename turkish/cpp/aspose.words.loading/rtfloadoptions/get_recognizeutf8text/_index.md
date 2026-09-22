---
title: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text yöntemi"
linktitle: "get_RecognizeUtf8Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text yöntemi. true olarak ayarlandığında, UTF8 karakterlerini algılamaya çalışır, bunlar C++'ta içe aktarım sırasında korunur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


**true** olarak ayarlandığında, UTF8 karakterlerini tespit etmeye çalışır ve içe aktarma sırasında korunur.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Açıklamalar


Varsayılan değer **false**'dır.

## Örnekler



Bir RTF belgesi yüklenirken UTF-8 karakterlerinin nasıl tespit edileceğini gösterir.
```cpp
// "RtfLoadOptions" nesnesi oluşturun, RTF belgesini nasıl yüklediğimizi değiştirmek için.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// "RecognizeUtf8Text" özelliğini "false" olarak ayarlayın, belgenin ISO 8859-1 karakter kümesini kullandığını varsaymak için
// ve belgedeki her karakteri yükler.
// "RecognizeUtf8Text" özelliğini "true" olarak ayarlayın, metinde ortaya çıkabilecek değişken uzunlukta karakterleri ayrıştırmak için.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## Ayrıca Bakınız

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
