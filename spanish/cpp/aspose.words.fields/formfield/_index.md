---
title: "Clase Aspose::Words::Fields::FormField"
linktitle: "FormField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FormField. Representa un único campo de formulario. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 112000
url: /es/cpp/aspose.words.fields/formfield/
---
## FormField class


Representa un solo campo de formulario. Para obtener más información, visite el artículo de documentación [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [get_CalculateOnExit](./get_calculateonexit/)() | Verdadero si las referencias al campo de formulario especificado se actualizan automáticamente cada vez que se sale del campo. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Obtiene o establece el tamaño de la casilla de verificación en puntos. Tiene efecto solo cuando [IsCheckBoxExactSize](./get_ischeckboxexactsize/) es **true**. |
| [get_Checked](./get_checked/)() | Obtiene o establece el estado marcado de la casilla de verificación del campo de formulario. El valor predeterminado para esta propiedad es **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| [get_Default](./get_default/)() | Obtiene o establece el valor predeterminado de la casilla de verificación del campo de formulario. El valor predeterminado para esta propiedad es **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtiene el documento al que pertenece este nodo. |
| [get_DropDownItems](./get_dropdownitems/)() | Proporciona acceso a los elementos de un campo de formulario desplegable. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Obtiene el índice que especifica el elemento actualmente seleccionado en un campo de formulario desplegable. |
| [get_Enabled](./get_enabled/)() | Verdadero si un campo de formulario está habilitado. |
| [get_EntryMacro](./get_entrymacro/)() | Devuelve o establece un nombre de macro de entrada para el campo de formulario. |
| [get_ExitMacro](./get_exitmacro/)() | Devuelve o establece un nombre de macro de salida para el campo de formulario. |
| [get_Font](../../aspose.words/inline/get_font/)() | Proporciona acceso al formato de fuente de este objeto. |
| [get_HelpText](./get_helptext/)() | Devuelve o establece el texto que se muestra en un cuadro de mensaje cuando el campo de formulario tiene el foco y el usuario pulsa F1. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Obtiene o establece el valor booleano que indica si el tamaño del cuadro de texto es automático o se especifica explícitamente. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Devuelve **true** si este nodo puede contener otros nodos. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Devuelve true si este objeto fue eliminado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Devuelve true si el formato del objeto se modificó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Devuelve true si este objeto fue insertado en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Devuelve **true** si este objeto fue movido (eliminado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Devuelve **true** si este objeto fue movido (insertado) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [get_MaxLength](./get_maxlength/)() | Longitud máxima para el campo de texto. Cero cuando la longitud no está limitada. |
| [get_Name](./get_name/)() | Obtiene o establece el nombre del campo de formulario. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Especifica la fuente del texto que se muestra en un cuadro de mensaje cuando un campo de formulario tiene el foco y el usuario pulsa F1. |
| [get_OwnStatus](./get_ownstatus/)() | Especifica la fuente del texto que se muestra en la barra de estado cuando un campo de formulario tiene el foco. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Recupera el [Paragraph](../../aspose.words/paragraph/) padre de este nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Devuelve un objeto [Range](../../aspose.words/range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_Result](./get_result/)() | Obtiene o establece una cadena que representa el resultado de este campo de formulario. |
| [get_StatusText](./get_statustext/)() | Devuelve o establece el texto que se muestra en la barra de estado cuando un campo de formulario tiene el foco. |
| [get_TextInputDefault](./get_textinputdefault/)() | Obtiene o establece la cadena predeterminada o una expresión de cálculo de un campo de formulario de texto. |
| [get_TextInputFormat](./get_textinputformat/)() | Devuelve o establece el formato de texto para un campo de formulario de texto. |
| [get_TextInputType](./get_textinputtype/)() | Obtiene el tipo de un campo de formulario de texto. |
| [get_Type](./get_type/)() | Devuelve el tipo de campo de formulario. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../../aspose.words/nodetype/) especificado. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Obtiene el carácter especial que representa este nodo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del nodo padre. |
| [RemoveField](./removefield/)() | Elimina el campo de formulario completo, no solo el carácter especial del campo de formulario. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | Método set para [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | Método set para [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | Método set para [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Método set para [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | Método set para [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Establece el índice que especifica el elemento actualmente seleccionado en un campo de formulario desplegable. |
| [set_Enabled](./set_enabled/)(bool) | Verdadero si un campo de formulario está habilitado. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | Método set para [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Setter para [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Longitud máxima para el campo de texto. Cero cuando la longitud no está limitada. |
| [set_Name](./set_name/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Setter para [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Setter para [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Setter para [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Establece el tipo de un campo de formulario de texto. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Aplica el formato de texto especificado en [TextInputFormat](./get_textinputformat/) y almacena el valor en [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
## Observaciones


Microsoft Word proporciona los siguientes campos de formulario: casilla de verificación, entrada de texto y lista desplegable (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Un campo de formulario completo en un documento de Word es una estructura compleja representada por varios nodos: inicio de campo, código de campo como FORMTEXT, datos del campo de formulario, separador de campo, resultado del campo, fin de campo y un marcador. Para crear programáticamente campos de formulario en un documento de Word use [InsertCheckBox()](../), [InsertTextInput()](../) y [InsertComboBox()](../) que aseguran que todos los nodos del campo de formulario se creen en el orden correcto y en un estado adecuado.

## Ejemplos



Muestra cómo insertar un cuadro combinado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Inserte un cuadro combinado que permitirá al usuario elegir una opción de una colección de cadenas.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// El campo de formulario aparecerá en forma de una etiqueta HTML "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Muestra cómo formatear todo el [FormField](./), incluido el valor del campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(0);
formField->get_Font()->set_Bold(true);
formField->get_Font()->set_Size(24);
formField->get_Font()->set_Color(System::Drawing::Color::get_Red());

formField->set_Result(u"Aspose.FormField");

doc = Aspose::Words::ApiExamples::DocumentHelper::SaveOpen(doc);

System::SharedPtr<Aspose::Words::Run> formFieldRun = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1);

ASSERT_EQ(u"Aspose.FormField", formFieldRun->get_Text());
ASPOSE_ASSERT_EQ(true, formFieldRun->get_Font()->get_Bold());
ASPOSE_ASSERT_EQ(24, formFieldRun->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), formFieldRun->get_Font()->get_Color().ToArgb());
```

## Ver también

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
