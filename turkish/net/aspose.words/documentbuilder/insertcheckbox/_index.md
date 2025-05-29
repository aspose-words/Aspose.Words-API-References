---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertCheckBox yöntemi ile etkileşimli onay kutusu form alanlarını zahmetsizce ekleyin ve belgelerinizde kullanıcı etkileşimini artırın.
type: docs
weight: 290
url: /tr/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

Geçerli konuma bir onay kutusu form alanı ekler.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değer kesilecektir. |
| checkedValue | Boolean | Onay kutusu form alanının durumu kontrol edildi. |
| size | Int32 | Onay kutusunun boyutunu puan olarak belirtir. MS Word için onay kutusunun boyutunu otomatik olarak hesaplamak üzere 0 belirtin. |

### Geri dönüş değeri

Az önce eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirttiğinizde, aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Belgeye onay kutularının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Farklı boyutlarda onay kutuları ve varsayılan işaretli durumları ekleyin.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Form alanlarının ad uzunluk sınırı 20 karakterdir.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Bu onay kutularıyla Microsoft Word'de çift tıklayarak etkileşime geçebiliriz.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Ayrıca bakınız

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

Geçerli konuma bir onay kutusu form alanı ekler.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değer kesilecektir. |
| defaultValue | Boolean | Onay kutusu form alanının varsayılan değeri. |
| checkedValue | Boolean | Onay kutusu form alanının şu anki işaretli durumu. |
| size | Int32 | Onay kutusunun boyutunu puan olarak belirtir. MS Word için onay kutusunun boyutunu otomatik olarak hesaplamak üzere 0 belirtin. |

### Geri dönüş değeri

Az önce eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirttiğinizde, aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Belgeye onay kutularının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Farklı boyutlarda onay kutuları ve varsayılan işaretli durumları ekleyin.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Form alanlarının ad uzunluk sınırı 20 karakterdir.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Bu onay kutularıyla Microsoft Word'de çift tıklayarak etkileşime geçebiliriz.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Ayrıca bakınız

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
