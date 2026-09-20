---
title: "Interfaz Aspose::Words::Fields::IBarcodeGenerator"
linktitle: "IBarcodeGenerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::Fields::IBarcodeGenerator. Interfaz pública para generador de códigos de barras personalizado. La implementación debe ser proporcionada por el usuario en C++."
type: docs
weight: 118000
url: /es/cpp/aspose.words.fields/ibarcodegenerator/
---
## IBarcodeGenerator interface


Interfaz pública para generador de códigos de barras personalizado. La implementación debe ser proporcionada por el usuario.

```cpp
class IBarcodeGenerator : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [GetBarcodeImage](./getbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Genera una imagen de código de barras usando el conjunto de parámetros (para el campo DisplayBarcode). |
| virtual [GetOldBarcodeImage](./getoldbarcodeimage/)(System::SharedPtr\<Aspose::Words::Fields::BarcodeParameters\>) | Genera una imagen de código de barras usando el conjunto de parámetros (para el campo Barcode tradicional). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
