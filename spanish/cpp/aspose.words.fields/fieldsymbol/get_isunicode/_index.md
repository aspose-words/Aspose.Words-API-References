---
title: "Aspose::Words::Fields::FieldSymbol::get_IsUnicode método"
linktitle: "get_IsUnicode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldSymbol::get_IsUnicode método. Obtiene o establece si el código de carácter se interpreta como el valor de un carácter Unicode en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.fields/fieldsymbol/get_isunicode/
---
## FieldSymbol::get_IsUnicode method


Obtiene o establece si el código de carácter se interpreta como el valor de un carácter Unicode.

```cpp
bool Aspose::Words::Fields::FieldSymbol::get_IsUnicode()
```


## Ejemplos



Muestra cómo usar el campo SYMBOL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan tres formas de usar un campo SYMBOL para mostrar un solo carácter.
// 1 -  Añade un campo SYMBOL que muestra el símbolo © (Copyright), especificado por un código de carácter ANSI:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// El código de carácter ANSI "U+00A9", o "169" en forma entera, está reservado para el símbolo de copyright.
field->set_CharacterCode(System::Convert::ToString(0x00a9));
field->set_IsAnsi(true);

ASSERT_EQ(u" SYMBOL  169 \\a", field->GetFieldCode());

builder->Writeln(u" Line 1");

// 2 -  Añade un campo SYMBOL que muestra el símbolo ∞ (Infinity), y modifica su apariencia:
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));

// En Unicode, el símbolo de infinito ocupa el código "221E".
field->set_CharacterCode(System::Convert::ToString(0x221E));
field->set_IsUnicode(true);

// Cambie la fuente de nuestro símbolo después de usar el Mapa de caracteres de Windows
// para asegurarse de que la fuente pueda representar ese símbolo.
field->set_FontName(u"Calibri");
field->set_FontSize(u"24");

// Podemos establecer esta bandera para símbolos altos para que no empujen hacia abajo el resto del texto en su línea.
field->set_DontAffectsLineSpacing(true);

ASSERT_EQ(u" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field->GetFieldCode());

builder->Writeln(u"Line 2");

// 3 -  Añadir un campo SYMBOL que muestre el carácter あ,
// con una fuente que soporte la página de códigos Shift-JIS (Windows-932):
field = System::ExplicitCast<Aspose::Words::Fields::FieldSymbol>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSymbol, true));
field->set_FontName(u"MS Gothic");
field->set_CharacterCode(System::Convert::ToString(0x82A0));
field->set_IsShiftJis(true);

ASSERT_EQ(u" SYMBOL  33440 \\f \"MS Gothic\" \\j", field->GetFieldCode());

builder->Write(u"Line 3");

doc->Save(get_ArtifactsDir() + u"Field.SYMBOL.docx");
```

## Ver también

* Class [FieldSymbol](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
