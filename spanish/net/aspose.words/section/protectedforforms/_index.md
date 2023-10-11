---
title: Section.ProtectedForForms
second_title: Referencia de API de Aspose.Words para .NET
description: Section propiedad. Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios los usuarios pueden seleccionar y modificar texto solo en los campos de formulario en Microsoft Word.
type: docs
weight: 60
url: /es/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios, los usuarios pueden seleccionar y modificar texto solo en los campos de formulario en Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

### Ejemplos

Muestra cómo desactivar la protección de una sección.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Aplicar protección contra escritura a cada sección del documento.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Desactiva la protección contra escritura para la primera sección.
doc.Sections[0].ProtectedForForms = false;

// En este documento de salida, podremos editar la primera sección libremente,
// y solo podremos editar el contenido del campo del formulario en la segunda sección.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ver también

* class [Section](../)
* espacio de nombres [Aspose.Words](../../section/)
* asamblea [Aspose.Words](../../../)


