---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words para .NET
description: Proteja sus documentos fácilmente con Document Protect. Evite cambios no autorizados manteniendo su contraseña intacta o usando una aleatoria.
type: docs
weight: 690
url: /es/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Protege el documento de cambios sin cambiar la contraseña existente o asigna una contraseña aleatoria.

```csharp
public void Protect(ProtectionType type)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| type | ProtectionType | Especifica el tipo de protección para el documento. |

## Observaciones

Cuando un documento está protegido, el usuario solo puede realizar cambios limitados, como agregar anotaciones, realizar revisiones o completar un formulario.

Cuando se protege un documento, y el documento ya tiene una contraseña de protección, la contraseña de protección existente no se cambia.

Cuando protege un documento y el documento no tiene una contraseña de protección, este método asigna una contraseña aleatoria que hace imposible desproteger el documento en Microsoft Word, pero aún puede desproteger el documento en Aspose.Words ya que no requiere una contraseña para desprotegerlo.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Protege el documento contra cambios y opcionalmente establece una contraseña de protección.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| type | ProtectionType | Especifica el tipo de protección para el documento. |
| password | String | La contraseña para proteger el documento con . Especificar`nulo` o cadena vacía si desea proteger el documento sin contraseña. |

## Observaciones

Cuando un documento está protegido, el usuario solo puede realizar cambios limitados, como agregar anotaciones, realizar revisiones o completar un formulario.

Tenga en cuenta que la protección del documento es diferente de la protección contra escritura. La protección contra escritura se especifica utilizando el[`WriteProtection`](../writeprotection/).

## Ejemplos

Muestra cómo proteger y desproteger un documento.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Si abrimos este documento con Microsoft Word con la intención de editarlo,
// Necesitaremos aplicar la contraseña para pasar la protección.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Tenga en cuenta que la protección solo se aplica a los usuarios de Microsoft Word que abren nuestro documento.
//No hemos cifrado el documento de ninguna manera y no necesitamos la contraseña para abrirlo y editarlo programáticamente.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Hay dos formas de eliminar la protección de un documento.
// 1 - Sin contraseña:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Con la contraseña correcta:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Ver también

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
