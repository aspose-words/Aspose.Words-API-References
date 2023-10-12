---
title: Document.Unprotect
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Elimina la protección del documento independientemente de la contraseña.
type: docs
weight: 760
url: /es/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Elimina la protección del documento independientemente de la contraseña.

```csharp
public void Unprotect()
```

### Observaciones

Este método desprotege el documento incluso si tiene una contraseña de protección.

Tenga en cuenta que la protección de documentos es diferente de la protección contra escritura. La protección contra escritura se especifica mediante el[`WriteProtection`](../writeprotection/).

### Ejemplos

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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)

---

## Unprotect(string) {#unprotect}

Elimina la protección del documento si se especifica una contraseña correcta.

```csharp
public bool Unprotect(string password)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| password | String | La contraseña con la que desproteger el documento. |

### Valor_devuelto

`verdadero` si se especificó una contraseña correcta y el documento estaba desprotegido.

### Observaciones

Este método desprotege el documento sólo si se especifica una contraseña correcta.

Tenga en cuenta que la protección de documentos es diferente de la protección contra escritura. La protección contra escritura se especifica mediante el[`WriteProtection`](../writeprotection/).

### Ejemplos

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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


