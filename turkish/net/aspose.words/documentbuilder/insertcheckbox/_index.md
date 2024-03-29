---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertCheckBox yöntem. Geçerli konuma bir onay kutusu form alanı ekler C#'da.
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
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun olan değer kesilecektir. |
| checkedValue | Boolean | Onay kutusu form alanının kontrol edilen durumu. |
| size | Int32 | Onay kutusunun boyutunu nokta cinsinden belirtir. Onay kutusunun boyutunu otomatik olarak hesaplamak için MS Word için 0 belirtin. |

### Geri dönüş değeri

Yeni eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirlerseniz aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Onay kutularının belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Farklı boyutlarda ve varsayılan kontrol durumlarında onay kutuları ekleyin.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Form alanlarının ad uzunluğu sınırı 20 karakterdir.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Microsoft Word'de bu onay kutularına çift tıklayarak etkileşim kurabiliriz.
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
| name | String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun olan değer kesilecektir. |
| defaultValue | Boolean | Onay kutusu form alanının varsayılan değeri. |
| checkedValue | Boolean | Onay kutusu form alanının mevcut kontrol durumu. |
| size | Int32 | Onay kutusunun boyutunu nokta cinsinden belirtir. Onay kutusunun boyutunu otomatik olarak hesaplamak için MS Word için 0 belirtin. |

### Geri dönüş değeri

Yeni eklenen form alanı düğümü.

## Notlar

Form alanı için bir ad belirlerseniz aynı adla otomatik olarak bir yer imi oluşturulur.

## Örnekler

Onay kutularının belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Farklı boyutlarda ve varsayılan kontrol durumlarında onay kutuları ekleyin.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Form alanlarının ad uzunluğu sınırı 20 karakterdir.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// Microsoft Word'de bu onay kutularına çift tıklayarak etkileşim kurabiliriz.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### Ayrıca bakınız

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
