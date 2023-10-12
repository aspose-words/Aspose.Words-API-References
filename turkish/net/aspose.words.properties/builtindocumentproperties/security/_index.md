---
title: BuiltInDocumentProperties.Security
second_title: Aspose.Words for .NET API Referansı
description: BuiltInDocumentProperties mülk. Bir belgenin güvenlik düzeyini sayısal bir değer olarak belirtir.
type: docs
weight: 250
url: /tr/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Bir belgenin güvenlik düzeyini sayısal bir değer olarak belirtir.

```csharp
public DocumentSecurity Security { get; set; }
```

### Notlar

Bu özelliği yalnızca bilgilendirme amacıyla kullanın, çünkü Microsoft Word bu özelliği her zaman ayarlamaz. Bu özellik yalnızca DOC ve OOXML belgelerinde mevcuttur.

Bir belgeyi korumak veya korumayı kaldırmak için the kullanın[`Protect`](../../../aspose.words/document/protect/) Ve[`Unprotect`](../../../aspose.words/document/unprotect/) yöntemler.

Aspose.Words, bir belgeyi kaydetmeden önce bu özelliği doğru bir değere günceller.

### Örnekler

Bir belgenin güvenlik düzeyini görüntülemek için belge özelliklerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Bir belgeyi salt okunur olacak şekilde yapılandırırsak, "Güvenlik" yerleşik özelliğini kullanarak bu durumu gösterecektir.
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Bir belgeyi yazmaya karşı koruyun ve ardından güvenlik düzeyini doğrulayın.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Güvenlik" açıklayıcı bir özelliktir. Değerini manuel olarak düzenleyebiliriz.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Ayrıca bakınız

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties/)
* toplantı [Aspose.Words](../../../)


