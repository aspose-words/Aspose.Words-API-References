---
title: "Интерфейс Aspose::Words::Fields::IBarcodeGenerator"
linktitle: "IBarcodeGenerator"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Fields::IBarcodeGenerator. Публичный интерфейс для пользовательского генератора штрихкода. Реализацию должен предоставить пользователь на C++."
type: docs
weight: 118000
url: /ru/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Публичный интерфейс для пользовательского генератора штрихкода. Реализацию должен предоставить пользователь.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Создайте изображение штрихкода, используя набор параметров (для поля DisplayBarcode). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Создайте изображение штрихкода, используя набор параметров (для традиционного поля Barcode). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
