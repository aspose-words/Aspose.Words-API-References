---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words para .NET
description: Document ProtectionType propiedad. Obtiene el tipo de protección del documento actualmente activo en C#.
type: docs
weight: 330
url: /es/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Obtiene el tipo de protección del documento actualmente activo.

```csharp
public ProtectionType ProtectionType { get; }
```

## Observaciones

Esta propiedad permite recuperar el tipo de protección de documento actualmente establecido. Para cambiar el tipo de protección de documento utilice el[`Protect`](../protect/) y[`Unprotect`](../unprotect/) métodos.

Cuando un documento está protegido, el usuario sólo puede realizar cambios limitados, , como agregar anotaciones, realizar revisiones o completar un formulario.

Tenga en cuenta que la protección de documentos es diferente de la protección contra escritura. La protección contra escritura se especifica mediante el[`WriteProtection`](../writeprotection/)

## Ejemplos

Muestra cómo proteger y desproteger un documento.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Si abrimos este documento con Microsoft Word con la intención de editarlo,
// necesitaremos aplicar la contraseña para superar la protección.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Tenga en cuenta que la protección sólo se aplica a los usuarios de Microsoft Word que abren nuestro documento.
// No hemos cifrado el documento de ninguna manera y no necesitamos la contraseña para abrirlo y editarlo mediante programación.
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
