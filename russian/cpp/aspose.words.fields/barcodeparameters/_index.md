---
title: "Aspose::Words::Fields::BarcodeParameters класс"
linktitle: "BarcodeParameters"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::BarcodeParameters класс. Класс‑контейнер для параметров штрих‑кода, передаваемых в BarcodeGenerator. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


Класс‑контейнер для параметров штрих‑кода, передаваемых в BarcodeGenerator. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class BarcodeParameters : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | Нужно ли добавлять символы начала/конца для типов штрих‑кодов NW7 и CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | Цвет фона штрих‑кода (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | Тип штрих‑кода. |
| [get_BarcodeValue](./get_barcodevalue/)() const | Данные для кодирования. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | Отображать ли данные штрих‑кода (текст) вместе с изображением. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | Уровень коррекции ошибок QR‑кода. Допустимые значения: [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | Тип маркера идентификации ориентации (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | Исправлять ли контрольную цифру, если она недействительна. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | Цвет переднего плана штрих‑кода (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | Является ли [PostalAddress](./get_postaladdress/) именем закладки. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | Является ли [PostalAddress](./get_postaladdress/) почтовым адресом США. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | Почтовый адрес штрих‑кода. |
| [get_ScalingFactor](./get_scalingfactor/)() const | Коэффициент масштабирования символа. Значение задаётся в целых процентах, допустимые значения: [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | Высота изображения штрих‑кода (в twips — 1/1440 дюйма) |
| [get_SymbolRotation](./get_symbolrotation/)() const | Поворот символа штрих‑кода. Допустимые значения: [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Нужно ли добавлять символы начала/конца для типов штрих‑кодов NW7 и CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Цвет фона штрих‑кода (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Тип штрих‑кода. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Данные для кодирования. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Отображать ли данные штрих‑кода (текст) вместе с изображением. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Уровень коррекции ошибок QR‑кода. Допустимые значения: [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | Тип маркера идентификации ориентации (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Исправлять ли контрольную цифру, если она недействительна. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Цвет переднего плана штрих‑кода (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | Является ли [PostalAddress](./get_postaladdress/) именем закладки. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | Является ли [PostalAddress](./get_postaladdress/) почтовым адресом США. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | Почтовый адрес штрих‑кода. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Коэффициент масштабирования символа. Значение задаётся в целых процентах, допустимые значения: [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Высота изображения штрих‑кода (в twips — 1/1440 дюйма) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Поворот символа штрих‑кода. Допустимые значения: [0, 3]. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
