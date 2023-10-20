---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words para .NET
description: BuiltInDocumentProperties Security propiedad. Especifica el nivel de seguridad de un documento como un valor numérico en C#.
type: docs
weight: 250
url: /es/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Especifica el nivel de seguridad de un documento como un valor numérico.

```csharp
public DocumentSecurity Security { get; set; }
```

## Observaciones

Utilice esta propiedad sólo con fines informativos porque Microsoft Word no siempre establece esta propiedad. Esta propiedad solo está disponible en documentos DOC y OOXML.

Para proteger o desproteger un documento utilice the [`Protect`](../../../aspose.words/document/protect/) y[`Unprotect`](../../../aspose.words/document/unprotect/) métodos.

Aspose.Words actualiza esta propiedad a un valor correcto antes de guardar un documento.

## Ejemplos

Muestra cómo utilizar las propiedades del documento para mostrar el nivel de seguridad de un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Si configuramos un documento para que sea de solo lectura, mostrará este estado usando la propiedad incorporada "Seguridad".
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Proteger contra escritura un documento y luego verificar su nivel de seguridad.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Seguridad" es una propiedad descriptiva. Podemos editar su valor manualmente.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Ver también

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
