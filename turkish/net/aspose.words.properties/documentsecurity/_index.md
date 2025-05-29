---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: .NET için Aspose.Words
description: Belgenizin güvenliğini artırmak için Aspose.Words.DocumentSecurity enum'unu keşfedin. En iyi koruma için güvenlik seviyelerini kolayca belirtin ve yönetin.
type: docs
weight: 5220
url: /tr/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Bir değer olarak kullanılır[`Security`](../builtindocumentproperties/security/) property. Bir belgenin güvenlik düzeyini sayısal bir değer olarak belirtir.

```csharp
[Flags]
public enum DocumentSecurity
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Özellik tarafından belirtilen herhangi bir güvenlik durumu yok. |
| PasswordProtected | `1` | Belge parola korumalıdır. (Not şimdiye kadar hiçbir belgede görülmemiştir). |
| ReadOnlyRecommended | `2` | Mümkünse salt okunur olarak açılacak belge, ancak ayar geçersiz kılınabilir. |
| ReadOnlyEnforced | `4` | Her zaman salt okunur olarak açılacak belge. |
| ReadOnlyExceptAnnotations | `8` | Açıklamalar hariç her zaman salt okunur olarak açılacak belge. |

## Örnekler

Bir belgenin güvenlik düzeyini görüntülemek için belge özelliklerinin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Bir belgeyi salt okunur olarak yapılandırırsak, bu durumu "Güvenlik" yerleşik özelliğini kullanarak görüntüler.
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

// "Güvenlik" tanımlayıcı bir özelliktir. Değerini manuel olarak düzenleyebiliriz.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)
