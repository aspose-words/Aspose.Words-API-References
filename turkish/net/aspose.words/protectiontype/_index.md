---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words for .NET
description: Aspose.Words.ProtectionType Sıralama. Bir belge için koruma türü C#'da.
type: docs
weight: 4510
url: /tr/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Bir belge için koruma türü.

```csharp
public enum ProtectionType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| AllowOnlyComments | `1` | Kullanıcı yalnızca belgedeki yorumları değiştirebilir. |
| AllowOnlyFormFields | `2` | Kullanıcı yalnızca belgedeki form alanlarına veri girebilir. |
| AllowOnlyRevisions | `0` | Kullanıcı belgeye yalnızca revizyon işaretleri ekleyebilir. |
| ReadOnly | `3` | Belgede değişiklik yapılmasına izin verilmez. Microsoft Word 2003. 'den beri mevcuttur |
| NoProtection | `-1` | Belge korunmuyor. |

## Örnekler

Bir bölüm için korumanın nasıl kapatılacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygulayın.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapatın.
doc.Sections[0].ProtectedForForms = false;

// Bu çıktı belgesinde ilk bölümü serbestçe düzenleyebileceğiz,
// ve ikinci bölümde sadece form alanının içeriğini düzenleyebileceğiz.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
