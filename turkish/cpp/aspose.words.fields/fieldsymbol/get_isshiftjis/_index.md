---
title: "Aspose::Words::Fields::FieldSymbol::get_IsShiftJis yöntemi"
linktitle: "get_IsShiftJis"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldSymbol::get_IsShiftJis yöntemi. Karakter kodunun bir SHIFT-JIS karakterinin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. C++."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fields/fieldsymbol/get_isshiftjis/
---
## FieldSymbol::get_IsShiftJis method


Karakter kodunun bir SHIFT-JIS karakter değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldSymbol::get_IsShiftJis()
```


## Örnekler



SYMBOL alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda tek bir karakteri görüntülemek için bir SYMBOL alanını kullanmanın üç yolu verilmiştir.
// 1 -  ANSI karakter kodu ile belirtilen © (Telif Hakkı) sembolünü gösteren bir SYMBOL alanı ekleyin:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// ANSI karakter kodu "U+00A9" veya tamsayı biçiminde "169", telif hakkı sembolü için ayrılmıştır.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  ∞ (Sonsuzluk) sembolünü gösteren bir SYMBOL alanı ekleyin ve görünümünü değiştirin:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// Unicode'da, sonsuzluk sembolü "221E" kodunu kaplar.
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Windows Karakter Haritası'nı kullandıktan sonra sembolümüzün yazı tipini değiştirin.
// yazı tipinin bu sembolü temsil edebildiğinden emin olmak için.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Uzun semboller için bu bayrağı ayarlayarak, satırdaki metnin geri kalanını aşağı itmelerini önleyebiliriz.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  あ karakterini gösteren bir SYMBOL alanı ekleyin,
// Shift-JIS (Windows-932) kod sayfasını destekleyen bir yazı tipiyle:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Ayrıca Bakınız

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
