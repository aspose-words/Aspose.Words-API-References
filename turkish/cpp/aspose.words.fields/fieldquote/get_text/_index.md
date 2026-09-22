---
title: "Aspose::Words::Fields::FieldQuote::get_Text yöntemi"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldQuote::get_Text yöntemi. C++'ta alınacak metni alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Alınacak metni alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Örnekler



QUOTE alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir QUOTE alanı ekleyin; bu, Text özelliğinin değerini görüntüler.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Bir QUOTE alanı ekleyin ve içine bir DATE alanı yerleştirin.
// DATE alanları, belgeyi Microsoft Word ile her açtığımızda değerlerini geçerli tarihe günceller.
// DATE alanını QUOTE alanının içine bu şekilde yerleştirmek, değerini dondurur
// belgeyi oluşturduğumuz tarihe.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Tüm alanları doğru sonuçlarını gösterecek şekilde güncelleyin.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## Ayrıca Bakınız

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
