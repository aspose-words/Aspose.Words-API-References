---
title: Document.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words para .NET
description: Descubra si su documento contiene macros de proyecto de VBA con la propiedad HasMacros. ¡Mejore la automatización y la eficiencia de sus flujos de trabajo hoy mismo!
type: docs
weight: 200
url: /es/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

Devuelve`verdadero` si el documento tiene un proyecto VBA (macros).

```csharp
public bool HasMacros { get; }
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

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
