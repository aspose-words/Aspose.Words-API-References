---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words para .NET
description: Descubra cómo personalizar la propiedad FieldMacroButton DisplayText para optimizar la ejecución de macros. ¡Configure el texto de botón perfecto para comandos de usuario fluidos!
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Obtiene o establece el texto que aparecerá como el "botón" que se selecciona para ejecutar la macro o el comando.

```csharp
public string DisplayText { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos MACROBUTTON para permitirnos ejecutar las macros de un documento haciendo clic.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Inserte un campo MACROBUTTON y haga referencia a una de las macros del documento por nombre en la propiedad MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Utilice la propiedad para hacer referencia a "ViewZoom200", una macro que viene con Microsoft Word.
//Podemos encontrar todas las demás macros a través de Ver -> Macros (desplegable) -> Ver Macros.
// En ese menú, seleccione "Comandos de Word" del menú desplegable "Macros en:".
// Si nuestro documento contiene una macro personalizada con el mismo nombre que una macro estándar,
//nuestra macro sera la que ejecute el campo MACROBUTTON.
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
