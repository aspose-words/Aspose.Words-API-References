---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FormField para crear y administrar fácilmente campos de formulario personalizables en sus documentos para una mejor interacción del usuario.
type: docs
weight: 3030
url: /es/net/aspose.words.fields/formfield/
---
## FormField class

Representa un solo campo de formulario.

Para obtener más información, visite el[Trabajar con campos de formulario](https://docs.aspose.com/words/net/working-with-form-fields/) Artículo de documentación.

```csharp
public class FormField : SpecialChar
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | Verdadero si las referencias al campo de formulario especificado se actualizan automáticamente cada vez que se sale del campo. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Obtiene o establece el tamaño de la casilla de verificación en puntos. Tiene efecto solo cuando[`IsCheckBoxExactSize`](./ischeckboxexactsize/) es`verdadero` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Obtiene o establece el estado marcado del campo de formulario de casilla de verificación. El valor predeterminado para esta propiedad es`FALSO` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica un identificador de nodo personalizado. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Obtiene o establece el valor predeterminado del campo de formulario de casilla de verificación. El valor predeterminado para esta propiedad es`FALSO` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Proporciona acceso a los elementos de un campo de formulario desplegable. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Obtiene o establece el índice que especifica el elemento seleccionado actualmente en un campo de formulario desplegable. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | Verdadero si un campo de formulario está habilitado. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Devuelve o establece un nombre de macro de entrada para el campo de formulario. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Devuelve o establece un nombre de macro de salida para el campo de formulario. |
| [Font](../../aspose.words/inline/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Devuelve o establece el texto que se muestra en un cuadro de mensaje cuando el campo de formulario tiene el foco y el usuario presiona F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Obtiene o establece el valor booleano que indica si el tamaño del cuadro de texto es automático o se especifica explícitamente. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devuelve`verdadero` si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Devuelve`verdadero` Si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Longitud máxima del campo de texto. Cero si la longitud es ilimitada. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Obtiene o establece el nombre del campo de formulario. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo inmediatamente siguiente a este nodo. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | DevuelveFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Especifica la fuente del texto que se muestra en un cuadro de mensaje cuando un campo de formulario tiene el foco y el usuario presiona F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Especifica la fuente del texto que se muestra en la barra de estado cuando un campo de formulario tiene el foco. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../../aspose.words/paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un[`Range`](../../aspose.words/range/)objeto que representa la porción de un documento que está contenida en este nodo. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Obtiene o establece una cadena que representa el resultado de este campo de formulario. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Devuelve o establece el texto que se muestra en la barra de estado cuando un campo de formulario tiene el foco. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Obtiene o establece la cadena predeterminada o una expresión de cálculo de un campo de formulario de texto. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Devuelve o establece el formato de texto para un campo de formulario de texto. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Obtiene o establece el tipo de un campo de formulario de texto. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Devuelve el tipo de campo de formulario. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Obtiene el primer ancestro del tipo de objeto especificado. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtiene el carácter especial que representa este nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el siguiente nodo según el algoritmo de recorrido del árbol de preorden. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Obtiene el nodo anterior según el algoritmo de recorrido del árbol de preorden. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Elimina el campo de formulario completo, no sólo el carácter especial del campo de formulario. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | Aplica el formato de texto especificado en[`TextInputFormat`](./textinputformat/) y almacena el valor en[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporta el contenido del nodo en una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporta el contenido del nodo en una cadena utilizando las opciones de guardado especificadas. |

## Observaciones

Microsoft Word proporciona los siguientes campos de formulario: casilla de verificación, entrada de texto y menú desplegable (cuadro combinado).

`FormField` es un nodo en línea y solo puede ser un hijo de[`Paragraph`](../../aspose.words/paragraph/).

`FormField` se representa en un documento mediante un carácter especial and posicionado como un carácter dentro de una línea de texto.

Un campo de formulario completo en un documento de Word es una estructura compleja representada por varios nodos: inicio, código (como FORMTEXT), datos, separador, resultado, fin y marcador. Para crear campos de formulario en un documento de Word mediante programación, utilice[`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) y [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/)which asegúrese de que todos los nodos del campo de formulario se creen en un orden correcto y en un estado adecuado.

## Ejemplos

Muestra cómo formatear todo el FormField, incluido el valor del campo.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

Muestra cómo insertar un cuadro combinado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Inserte un cuadro combinado que permitirá al usuario elegir una opción de una colección de cadenas.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

//El campo de formulario aparecerá en forma de una etiqueta html "select".
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Ver también

* class [SpecialChar](../../aspose.words/specialchar/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
