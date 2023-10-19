---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl sınıf. Microsoft Forms 2.0 OLE kontrolünü temsil eder C#'da.
type: docs
weight: 1110
url: /tr/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Microsoft Forms 2.0 OLE kontrolünü temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-ole-objects/) dokümantasyon makalesi.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Denetimin Altyazı özelliğini alır. Varsayılan değer boş bir dizedir. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Anlık alt kontrollerin toplanmasını alır. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | İadeler`doğru` kontrol etkin durumdaysa. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Birbirini dışlayan denetimlerden oluşan bir grubu belirten bir dize alır veya ayarlar. Varsayılan değer boş bir dizedir. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | İadeler`doğru` eğer kontrol bir`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | ActiveX denetiminin adını alır veya ayarlar. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Forms 2.0 kontrolünün türünü alır. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Genellikle kontrol durumunu temsil eden temel Değer özelliğini alır. Örneğin işaretli seçenek düğmesi '1' değerine sahipken, işaretlenmemişse '0' değerine sahiptir. Varsayılan değer boş bir dizedir. |

## Örnekler

ActiveX denetiminin özelliklerinin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Bir Çerçeve için GrupAdı'nı ayarlayamayacağınızı unutmayın.
    checkBox.GroupName = "Aspose group name";
}
```

### Ayrıca bakınız

* class [OleControl](../olecontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
