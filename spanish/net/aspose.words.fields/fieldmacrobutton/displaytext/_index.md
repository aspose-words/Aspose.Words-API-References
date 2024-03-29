---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words para .NET
description: FieldMacroButton DisplayText propiedad. Obtiene o establece el texto para que aparezca como el botón seleccionado para ejecutar la macro o el comando en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Obtiene o establece el texto para que aparezca como el "botón" seleccionado para ejecutar la macro o el comando.

```csharp
public string DisplayText { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos MACROBUTTON para permitirnos ejecutar las macros de un documento haciendo clic.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Inserte un campo MACROBUTTON y haga referencia a una de las macros del documento por su nombre en la propiedad MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilice la propiedad para hacer referencia a "ViewZoom200", una macro que se incluye con Microsoft Word.
// Podemos encontrar todas las demás macros a través de Ver -> Macros (desplegable) -> Ver macros.
// En ese menú, seleccione "Comandos de Word" en el menú desplegable "Macros en:".
// Si nuestro documento contiene una macro personalizada con el mismo nombre que una macro de valores,
// nuestra macro será la que ejecute el campo MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Guarde el documento como un tipo de documento habilitado para macros.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Ver también

* class [FieldMacroButton](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
