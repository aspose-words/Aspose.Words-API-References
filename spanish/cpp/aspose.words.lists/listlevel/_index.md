---
title: "Clase Aspose::Words::Lists::ListLevel"
linktitle: "ListLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Lists::ListLevel. Define el formato para un nivel de lista. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Define el formato para un nivel de lista. Para obtener más información, visite el artículo de documentación [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Crea una forma de viñeta de imagen para el nivel de lista actual. |
| [DeletePictureBullet](./deletepicturebullet/)() | Elimina la viñeta de imagen del nivel de lista actual. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Compara con el [ListLevel](./) especificado. |
| [get_Alignment](./get_alignment/)() const | Obtiene o establece la justificación del número real del elemento de lista. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Obtiene o establece el formato de estilo de número personalizado para este nivel de lista. Por ejemplo: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Especifica el formato de carácter usado para la etiqueta de la lista. |
| [get_ImageData](./get_imagedata/)() | Devuelve los datos de imagen de la forma de viñeta de imagen para el nivel de lista actual. |
| [get_IsLegal](./get_islegal/)() const | True si el nivel convierte todos los números heredados a arábigos, false si conserva su estilo de número. |
| [get_LinkedStyle](./get_linkedstyle/)() | Obtiene o establece el estilo de párrafo que está vinculado a este nivel de lista. |
| [get_NumberFormat](./get_numberformat/)() const | Devuelve o establece el formato de número para el nivel de lista. |
| [get_NumberPosition](./get_numberposition/)() const | Devuelve o establece la posición (en puntos) del número o viñeta para el nivel de lista. |
| [get_NumberStyle](./get_numberstyle/)() const | Devuelve o establece el estilo de número para este nivel de lista. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Establece o devuelve el nivel de lista que debe aparecer antes de que el nivel de lista especificado reinicie la numeración. |
| [get_StartAt](./get_startat/)() | Devuelve o establece el número inicial para este nivel de lista. |
| [get_TabPosition](./get_tabposition/)() const | Devuelve o establece la posición de tabulación (en puntos) para el nivel de lista. |
| [get_TextPosition](./get_textposition/)() const | Devuelve o establece la posición (en puntos) para la segunda línea de texto de ajuste para el nivel de lista. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Devuelve o establece el carácter insertado después del número para el nivel de lista. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Informa la representación en cadena del objeto [ListLevel](./) para el índice especificado del elemento de lista. Los parámetros especifican el [NumberStyle](../../aspose.words/numberstyle/) y una cadena de formato opcional usada cuando se especifica [Custom](../../aspose.words/numberstyle/). |
| [GetHashCode](./gethashcode/)() const override | Calcula el código hash para este objeto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Elimina la tabulación del nivel de lista. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Método setter para [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | Método setter para [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | Método setter para [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Método setter para [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | Método setter para [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | Método setter para [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Método setter para [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Método setter para [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | Método setter para [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | Método setter para [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | Método setter para [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Método setter para [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## Observaciones


No crea objetos de esta clase. Los objetos de nivel [List](../list/) se crean automáticamente cuando se crea una lista. Accede a los objetos [ListLevel](./) a través de la colección [ListLevelCollection](../listlevelcollection/).

Utilice las propiedades de [ListLevel](./) para especificar el formato de lista para niveles de lista individuales.

## Ejemplos



Muestra cómo aplicar formato de lista personalizado a los párrafos al usar [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de la lista.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Este valor NumberFormat creará símbolos de viñetas en forma de estrella.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Cree párrafos y aplique ambos niveles de lista de nuestro formato de lista personalizado a ellos.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Ver también

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
