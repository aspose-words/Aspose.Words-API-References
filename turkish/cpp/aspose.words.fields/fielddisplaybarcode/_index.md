---
title: "Aspose::Words::Fields::FieldDisplayBarcode sınıfı"
linktitle: "FieldDisplayBarcode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldDisplayBarcode sınıfı. DISPLAYBARCODE alanını uygular. Daha fazla bilgi için C++ belgelerindeki makaleyi ziyaret edin."
type: docs
weight: 34000
url: /tr/cpp/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class


DISPLAYBARCODE alanını uygular. Daha fazla bilgi edinmek için, [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldDisplayBarcode : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | NW7 ve CODE39 barkod türleri için Başlat/Durdur karakterleri eklenip eklenmeyeceğini alır veya ayarlar. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Barkod sembolünün arka plan rengini alır veya ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır. |
| [get_BarcodeType](./get_barcodetype/)() | Barkod türünü (QR vb.) alır veya ayarlar. |
| [get_BarcodeValue](./get_barcodevalue/)() | Barkod değerini alır veya ayarlar. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_DisplayText](./get_displaytext/)() | Barkod verilerini (metni) görüntüyle birlikte gösterip göstermeyeceğini alır veya ayarlar. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | QR Kodunun hata düzeltme seviyesini alır veya ayarlar. Geçerli değerler [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Kontrol rakamı geçersizse düzeltileceğini alır veya ayarlar. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Barkod sembolünün ön plan rengini alır veya ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets or sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_ScalingFactor](./get_scalingfactor/)() | Sembol için ölçek faktörünü alır veya ayarlar. Değer tam yüzde puanlarıdır ve geçerli değerler [10, 1000] arasındadır. |
| [get_Separator](../field/get_separator/)() | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_SymbolHeight](./get_symbolheight/)() | Sembol yüksekliğini alır veya ayarlar. Birimler TWIPS'tir (1/1440 inç). |
| [get_SymbolRotation](./get_symbolrotation/)() | Barkod sembolünün dönüşünü alır veya ayarlar. Geçerli değerler [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_AddStartStopChar](./get_addstartstopchar/). |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_BackgroundColor](./get_backgroundcolor/). |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeType](./get_barcodetype/). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue](./get_barcodevalue/). |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle](./get_casecodestyle/). |
| [set_DisplayText](./set_displaytext/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_DisplayText](./get_displaytext/). |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_ErrorCorrectionLevel](./get_errorcorrectionlevel/). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_FixCheckDigit](./get_fixcheckdigit/). |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor](./get_foregroundcolor/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle](./get_poscodestyle/). |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_ScalingFactor](./get_scalingfactor/). |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight](./get_symbolheight/). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolRotation](./get_symbolrotation/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |

## Örnekler



DISPLAYBARCODE alanının nasıl ekleneceğini ve özelliklerinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Aşağıda, DISPLAYBARCODE alanının görüntüleyebileceği, çeşitli şekillerde süslenmiş dört barkod türü yer almaktadır.
// 1 -  Özel renklerle QR kodu:
field->set_BarcodeType(u"QR");
field->set_BarcodeValue(u"ABC123");
field->set_BackgroundColor(u"0xF8BD69");
field->set_ForegroundColor(u"0xB5413B");
field->set_ErrorCorrectionLevel(u"3");
field->set_ScalingFactor(u"250");
field->set_SymbolHeight(u"1000");
field->set_SymbolRotation(u"0");

ASSERT_EQ(u" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field->GetFieldCode());
builder->Writeln();

// 2 -  Çubukların altında rakamları gösterilen EAN13 barkodu:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  CODE39 barkodu:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  ITF4 barkod, belirtilen bir kasa kodu ile:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
