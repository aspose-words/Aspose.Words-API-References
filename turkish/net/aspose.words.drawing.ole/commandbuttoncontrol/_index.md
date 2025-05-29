---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: .NET için Aspose.Words
description: Uygulamalarınızda kullanıcı etkileşimini artırarak makroları çalıştıran etkileşimli düğmeler oluşturmak için Aspose.Words.Drawing.Ole.CommandButtonControl sınıfını keşfedin.
type: docs
weight: 1450
url: /tr/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

CommandButton denetimi, kullanıcı tıkladığında bir eylem gerçekleştiren bir makroyu çalıştırır.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Yeni bir örneğini başlatır`CommandButtonControl` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Denetimin arka plan rengini alır veya ayarlar. Varsayılan değer denetimin türüne bağlıdır. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Denetimin Başlık özelliğini alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Hemen alt kontrollerin koleksiyonunu alır. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Geri Döndürür`doğru` eğer kontrol etkin durumdaysa. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Denetimin ön plan rengini alır veya ayarlar. Varsayılan değer, denetimin türüne bağlıdır. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Karşılıklı olarak birbirini dışlayan denetimlerden oluşan bir grubu belirten bir dize alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Kontrolün yüksekliğini noktalar halinde alır veya ayarlar. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Geri Döndürür`doğru` eğer kontrol bir[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Forms 2.0 denetiminin türünü alır. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Genellikle kontrol durumunu temsil eden temel Değer özelliğini alır. Örneğin işaretli seçenek düğmesi '1' değerine sahipken, işaretsiz düğme '0' değerine sahiptir. Varsayılan değer boş bir dizedir. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Kontrolün genişliğini noktalar halinde alır veya ayarlar. |

## Örnekler

ActiveX denetiminin nasıl ekleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Ayrıca bakınız

* class [Forms2OleControl](../forms2olecontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
