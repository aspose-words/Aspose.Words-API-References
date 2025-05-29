---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ProtectedForForms en Microsoft Word mejora la seguridad del documento, permitiendo a los usuarios editar fácilmente únicamente los campos de formulario designados.
type: docs
weight: 60
url: /es/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios, los usuarios solo pueden seleccionar y modificar texto en los campos de formulario de Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

## Ejemplos

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

// Desactive la protección contra escritura para la primera sección.
doc.Sections[0].ProtectedForForms = false;

//En este documento de salida, podremos editar la primera sección libremente,
// y solo podremos editar el contenido del campo de formulario en la segunda sección.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ver también

* class [Section](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
