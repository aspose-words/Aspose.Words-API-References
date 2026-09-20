---
title: "Aspose::Words::Fields::FieldMergeBarcode class"
linktitle: "FieldMergeBarcode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldMergeBarcode class. Реализует поле MERGEBARCODE. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 66000
url: /ru/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


Реализует поле MERGEBARCODE. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Получает, следует ли добавлять символы Start/Stop для типов штрихкодов NW7 и CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Получает цвет фона символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Получает тип штрихкода (QR и др.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Получает значение штрихкода. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_DisplayText](./get_displaytext/)() | Получает, отображать ли данные штрихкода (текст) вместе с изображением. |
| [get_End](./get_end/)() override | Получает узел, представляющий конец поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Получает уровень коррекции ошибок QR‑кода. Допустимые значения — [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Получает, исправлять ли контрольную цифру, если она недействительна. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Получает цвет переднего плана символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_ScalingFactor](./get_scalingfactor/)() | Получает коэффициент масштабирования символа. Значение задаётся в целых процентах, допустимые значения — [10, 1000]. |
| [get_Separator](./get_separator/)() override | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](./get_start/)() override | Получает узел, представляющий начало поля. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_SymbolHeight](./get_symbolheight/)() | Получает высоту символа. Единицы измерения — TWIPS (1/1440 дюйма). |
| [get_SymbolRotation](./get_symbolrotation/)() | Получает вращение символа штрихкода. Допустимые значения — [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Устанавливает, следует ли добавлять символы Start/Stop для типов штрихкодов NW7 и CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Устанавливает цвет фона символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Устанавливает тип штрихкода (QR и др.). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Устанавливает значение штрихкода. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | Устанавливает, отображать ли данные штрихкода (текст) вместе с изображением. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Устанавливает уровень коррекции ошибок QR‑кода. Допустимые значения — [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Устанавливает, исправлять ли контрольную цифру, если она недействительна. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Устанавливает цвет переднего плана символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Устанавливает коэффициент масштабирования для символа. Значение задаётся в целых процентных пунктах, допустимые значения — [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Устанавливает высоту символа. Единицы измерения — TWIPS (1/1440 дюйма). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Устанавливает поворот штрихкода. Допустимые значения — [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
