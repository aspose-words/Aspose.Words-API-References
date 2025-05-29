---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: .NET için Aspose.Words
description: Onay kutusu değerlerini kolayca açıp kapatmak ve kusursuz entegrasyonla belge otomasyonunuzu geliştirmek için Aspose.Words.Drawing.Ole.CheckBoxControl sınıfını keşfedin.
type: docs
weight: 1440
url: /tr/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

CheckBox denetimi bir değeri değiştirir.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Denetimin arka plan rengini alır veya ayarlar. Varsayılan değer denetimin türüne bağlıdır. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Denetimin Başlık özelliğini alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Bu değeri belirten bir Boole değeri alır veya ayarlar`CheckBoxControl` işaretli mi değil mi? Varsayılan değer`YANLIŞ` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Hemen alt kontrollerin koleksiyonunu alır. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Geri Döndürür`doğru` eğer kontrol etkin durumdaysa. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Denetimin ön plan rengini alır veya ayarlar. Varsayılan değer, denetimin türüne bağlıdır. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Karşılıklı olarak birbirini dışlayan denetimlerden oluşan bir grubu belirten bir dize alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Kontrolün yüksekliğini noktalar halinde alır veya ayarlar. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Geri Döndürür`doğru` eğer kontrol bir[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Forms 2.0 denetiminin türünü alır. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Genellikle kontrol durumunu temsil eden temel Değer özelliğini alır. Örneğin işaretli seçenek düğmesi '1' değerine sahipken, işaretsiz düğme '0' değerine sahiptir. Varsayılan değer boş bir dizedir. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Kontrolün genişliğini noktalar halinde alır veya ayarlar. |

## Notlar

Üç olası durumu vardır: seçili, temizlenmiş ve ne seçili ne de temizlenmiş. açık ve kapalı durumlarının bir kombinasyonu anlamına gelir.

## Örnekler

CheckBox denetiminin durumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Ayrıca bakınız

* class [MorphDataControl](../morphdatacontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
