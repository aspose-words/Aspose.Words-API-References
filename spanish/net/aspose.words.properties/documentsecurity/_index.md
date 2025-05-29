---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.DocumentSecurity para mejorar la seguridad de sus documentos. Especifique y administre fácilmente los niveles de seguridad para una protección óptima.
type: docs
weight: 5220
url: /es/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Se utiliza como valor para el[`Security`](../builtindocumentproperties/security/) propiedad. Especifica el nivel de seguridad de un documento como un valor numérico.

```csharp
[Flags]
public enum DocumentSecurity
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No hay estados de seguridad especificados por la propiedad. |
| PasswordProtected | `1` | El documento está protegido con contraseña. (Esta nota nunca se ha visto en ningún documento hasta ahora). |
| ReadOnlyRecommended | `2` | El documento se abrirá en modo de solo lectura si es posible, pero la configuración se puede anular. |
| ReadOnlyEnforced | `4` | El documento siempre se abrirá en modo de solo lectura. |
| ReadOnlyExceptAnnotations | `8` | El documento siempre se abrirá en modo de solo lectura, excepto para las anotaciones. |

## Ejemplos

Muestra cómo utilizar las propiedades del documento para mostrar el nivel de seguridad de un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Si configuramos un documento para que sea de sólo lectura, mostrará este estado utilizando la propiedad incorporada "Seguridad".
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

* espacio de nombres [Aspose.Words.Properties](../../aspose.words.properties/)
* asamblea [Aspose.Words](../../)
