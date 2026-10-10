---
title: "Aspose::Words::Fields::FieldMacroButton::get_DisplayText método"
linktitle: "get_DisplayText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldMacroButton::get_DisplayText método. Obtiene o establece el texto que aparecerá como el \"botón\" que se selecciona para ejecutar la macro o comando en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldmacrobutton/get_displaytext/
---
## FieldMacroButton::get_DisplayText method


Obtiene o establece el texto que aparecerá como el "botón" que se selecciona para ejecutar la macro o el comando.

```cpp
System::String Aspose::Words::Fields::FieldMacroButton::get_DisplayText()
```


## Ejemplos



Muestra cómo usar los campos MACROBUTTON para permitir ejecutar las macros de un documento al hacer clic.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// Inserte un campo MACROBUTTON y haga referencia a una de las macros del documento por su nombre en la propiedad MacroName.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// Utilice la propiedad para hacer referencia a "ViewZoom200", una macro que se incluye con Microsoft Word.
// Podemos encontrar todas las demás macros a través de Ver -> Macros (desplegable) -> Ver macros.
// En ese menú, seleccione "Word Commands" del desplegable "Macros en:".
// Si nuestro documento contiene una macro personalizada con el mismo nombre que una macro estándar,
// nuestra macro será la que ejecute el campo MACROBUTTON.
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// Guarde el documento como un tipo de documento habilitado para macros.
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## Ver también

* Class [FieldMacroButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
