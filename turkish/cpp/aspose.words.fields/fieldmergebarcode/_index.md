---
title: "Aspose::Words::Fields::FieldMergeBarcode sınıfı"
linktitle: "FieldMergeBarcode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldMergeBarcode sınıfı. MERGEBARCODE alanını uygular. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 66000
url: /tr/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


MERGEBARCODE alanını uygular. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterleri eklenip eklenmeyeceğini alır. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Barkod sembolünün arka plan rengini alır. Geçerli değerler [0, 0xFFFFFF] aralığındadır. |
| [get_BarcodeType](./get_barcodetype/)() | Barkod tipini (QR vb.) alır. |
| [get_BarcodeValue](./get_barcodevalue/)() | Barkod değerini alır. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Görüntülenen alan sonucunu temsil eden metni alır. |
| [get_DisplayText](./get_displaytext/)() | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceğini alır. |
| [get_End](./get_end/)() override | Alan sonunu temsil eden düğümü alır. |
| [get_End](../field/get_end/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | QR Kodunun hata düzeltme seviyesini alır. Geçerli değerler [0, 3] arasındadır. |
| [get_FieldEnd](../field/get_fieldend/)() const | Alan sonunu temsil eden düğümü alır. |
| [get_FieldStart](../field/get_fieldstart/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Kontrol rakamı geçersizse düzeltileceğini alır. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Barkod sembolünün ön plan rengini alır. Geçerli değerler [0, 0xFFFFFF] aralığındadır. |
| [get_Format](../field/get_format/)() | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../fieldformat/) nesnesi alır. |
| [get_IsDirty](../field/get_isdirty/)() | Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [get_IsLocked](../field/get_islocked/)() | Alan'ın kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır veya ayarlar. |
| [get_LocaleId](../field/get_localeid/)() | Alan'ın LCID'sini alır veya ayarlar. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [get_ScalingFactor](./get_scalingfactor/)() | Sembol için bir ölçekleme faktörünü alır. Değer tam yüzde puanlarıdır ve geçerli değerler [10, 1000] arasındadır. |
| [get_Separator](./get_separator/)() override | Alan ayırıcıyı temsil eden düğümü alır. **null** olabilir. |
| [get_Start](./get_start/)() override | Alan başlangıcını temsil eden düğümü alır. |
| [get_Start](../field/get_start/)() const | Alan başlangıcını temsil eden düğümü alır. |
| [get_SymbolHeight](./get_symbolheight/)() | Sembolün yüksekliğini alır. Birimler TWIPS cinsindendir (1/1440 inç). |
| [get_SymbolRotation](./get_symbolrotation/)() | Barkod sembolünün dönüşünü alır. Geçerli değerler [0, 3] arasındadır. |
| virtual [get_Type](../field/get_type/)() const | Microsoft Word alan türünü alır. |
| [GetFieldCode](../field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Alanı belgeden kaldırır. Alanın hemen sonrasındaki bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafını döndürür. Alan zaten kaldırılmışsa, **null** döndürür. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterleri eklenip eklenmeyeceğini ayarlar. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Barkod sembolünün arka plan rengini ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Barkod tipini (QR vb.) ayarlar. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Barkod değerini ayarlar. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Barkod verisinin (metin) görüntüyle birlikte gösterilip gösterilmeyeceğini ayarlar. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | QR Kodunun hata düzeltme seviyesini ayarlar. Geçerli değerler [0, 3] arasındadır. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Kontrol rakamı geçersizse düzeltileceğini ayarlar. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Barkod sembolünün ön plan rengini ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır. |
| [set_IsDirty](../field/set_isdirty/)(bool) | [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) için ayarlayıcı. |
| [set_IsLocked](../field/set_islocked/)(bool) | [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) için ayarlayıcı. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) için ayarlayıcı. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | [Aspose::Words::Fields::Field::get_Result](../field/get_result/) için ayarlayıcı. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Sembol için bir ölçek faktörü ayarlar. Değer tam yüzde puanları cinsindendir ve geçerli değerler [10, 1000] arasındadır. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Sembolün yüksekliğini ayarlar. Birimler TWIPS (1/1440 inç) cinsindendir. |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Barkod sembolünün dönüşünü ayarlar. Geçerli değerler [0, 3] arasındadır. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Alan bağlantısını kaldırır. |
| [Update](../field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
| [Update](../field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır. |
## Ayrıca Bakınız

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
