---
title: "Класс Aspose::Words::Fields::FieldDisplayBarcode"
linktitle: "FieldDisplayBarcode"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Fields::FieldDisplayBarcode. Реализует поле DISPLAYBARCODE. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class


Реализует поле DISPLAYBARCODE. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldDisplayBarcode : public Aspose::Words::Fields::Field,
                            public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | Получает или задает, следует ли добавлять символы Start/Stop для типов штрихкодов NW7 и CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | Получает или задает цвет фона символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | Получает или задает тип штрихкода (QR и др.). |
| [get_BarcodeValue](./get_barcodevalue/)() | Получает или задает значение штрихкода. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_DisplayText](./get_displaytext/)() | Получает или задает, отображать ли данные штрихкода (текст) вместе с изображением. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | Получает или задает уровень коррекции ошибок QR‑кода. Допустимые значения: [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | Получает или задает, исправлять ли контрольную цифру, если она недействительна. |
| [get_ForegroundColor](./get_foregroundcolor/)() | Получает или задает цвет переднего плана символа штрихкода. Допустимые значения находятся в диапазоне [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets or sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_ScalingFactor](./get_scalingfactor/)() | Получает или задает коэффициент масштабирования символа. Значение задаётся в целых процентах, допустимые значения: [10, 1000]. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_SymbolHeight](./get_symbolheight/)() | Получает или задает высоту символа. Единицы измерения — TWIPS (1/1440 дюйма). |
| [get_SymbolRotation](./get_symbolrotation/)() | Получает или задает вращение символа штрихкода. Допустимые значения: [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_AddStartStopChar](./get_addstartstopchar/). |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_BackgroundColor](./get_backgroundcolor/). |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeType](./get_barcodetype/). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_BarcodeValue](./get_barcodevalue/). |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_CaseCodeStyle](./get_casecodestyle/). |
| [set_DisplayText](./set_displaytext/)(bool) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_DisplayText](./get_displaytext/). |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_ErrorCorrectionLevel](./get_errorcorrectionlevel/). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_FixCheckDigit](./get_fixcheckdigit/). |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_ForegroundColor](./get_foregroundcolor/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_PosCodeStyle](./get_poscodestyle/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_ScalingFactor](./get_scalingfactor/). |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolHeight](./get_symbolheight/). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldDisplayBarcode::get_SymbolRotation](./get_symbolrotation/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как вставить поле DISPLAYBARCODE и задать его свойства.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));

// Ниже представлены четыре типа штрихкодов, оформленных различными способами, которые может отображать поле DISPLAYBARCODE.
// 1 -  QR‑код с пользовательскими цветами:
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

// 2 -  Штрихкод EAN13, цифры отображаются под полосами:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"EAN13");
field->set_BarcodeValue(u"501234567890");
field->set_DisplayText(true);
field->set_PosCodeStyle(u"CASE");
field->set_FixCheckDigit(true);

ASSERT_EQ(u" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field->GetFieldCode());
builder->Writeln();

// 3 -  Штрихкод CODE39:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"CODE39");
field->set_BarcodeValue(u"12345ABCDE");
field->set_AddStartStopChar(true);

ASSERT_EQ(u" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field->GetFieldCode());
builder->Writeln();

// 4 -  штрих‑код ITF4 с указанным кодом корпуса:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDisplayBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDisplayBarcode, true));
field->set_BarcodeType(u"ITF14");
field->set_BarcodeValue(u"09312345678907");
field->set_CaseCodeStyle(u"STD");

ASSERT_EQ(u" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.DISPLAYBARCODE.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
