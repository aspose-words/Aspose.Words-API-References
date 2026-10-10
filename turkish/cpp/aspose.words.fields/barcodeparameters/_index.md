---
title: "Aspose::Words::Fields::BarcodeParameters sınıfı"
linktitle: "BarcodeParameters"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::BarcodeParameters sınıfı. BarcodeGenerator'a geçiş için barkod parametrelerini içeren kapsayıcı sınıf. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


BarcodeGenerator'a aktarılacak barkod parametreleri için kapsayıcı sınıf. Daha fazla bilgi için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class BarcodeParameters : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterleri eklenip eklenmeyeceği. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Barkod arka plan rengi (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Barkod tipi. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Kodlanacak veri. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Barkod verilerini (metin) görüntüyle birlikte gösterip göstermeyeceği. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | QR Kodunun hata düzeltme seviyesi. Geçerli değerler [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Facing Identification Mark (FIM) türü. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Kontrol rakamı geçersizse düzeltip düzeltmeyeceği. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Barkod ön plan rengi (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Bu [PostalAddress](./get_postaladdress/) bir yer imi adı mı. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Bu [PostalAddress](./get_postaladdress/) bir ABD posta adresi mi. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Barkod posta adresi. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Sembol için ölçek faktörü. Değer tam yüzde puanlarıyla verilir ve geçerli değerler [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Barkod görüntü yüksekliği (twip cinsinden - 1/1440 inç) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Barkod sembolünün dönüşü. Geçerli değerler [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | NW7 ve CODE39 barkod tipleri için Başlangıç/Bitiş karakterleri eklenip eklenmeyeceği. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Barkod arka plan rengi (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Barkod tipi. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Kodlanacak veri. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Barkod verilerini (metin) görüntüyle birlikte gösterip göstermeyeceği. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | QR Kodunun hata düzeltme seviyesi. Geçerli değerler [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Facing Identification Mark (FIM) türü. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Kontrol rakamı geçersizse düzeltip düzeltmeyeceği. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Barkod ön plan rengi (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Bu [PostalAddress](./get_postaladdress/) bir yer imi adı mı. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Bu [PostalAddress](./get_postaladdress/) bir ABD posta adresi mi. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Barkod posta adresi. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Sembol için ölçek faktörü. Değer tam yüzde puanlarıyla verilir ve geçerli değerler [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Barkod görüntü yüksekliği (twip cinsinden - 1/1440 inç) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Barkod sembolünün dönüşü. Geçerli değerler [0, 3]. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
