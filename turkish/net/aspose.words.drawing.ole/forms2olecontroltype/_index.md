---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: .NET için Aspose.Words
description: Gelişmiş belge otomasyonu için çeşitli Forms 2.0 kontrol türlerini içeren Aspose.Words.Drawing.Ole.Forms2OleControlType enum'unu keşfedin.
type: docs
weight: 1480
url: /tr/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Forms 2.0 denetimlerinin türlerini sıralar.

```csharp
public enum Forms2OleControlType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| OptionButton | `0` | Bir radyo düğmesi kontrolü. |
| Label | `1` | Metni görüntüleyen bir denetim. |
| Textbox | `2` | Kullanıcının metin girmesine izin veren bir denetim. |
| CheckBox | `3` | Kullanıcının bir seçeneği seçmesine veya seçimini kaldırmasına olanak tanıyan bir denetim. |
| ToggleButton | `4` | Kullanıcının iki durum arasında geçiş yapmasına olanak tanıyan bir denetim. |
| SpinButton | `5` | Kullanıcının bir değeri artırmasına veya azaltmasına izin veren bir denetim. |
| ComboBox | `6` | Kullanıcının bir listeden bir öğe seçmesine izin veren bir denetim. |
| Frame | `7` | Diğer denetimleri gruplandıran bir denetim. |
| MultiPage | `8` | Birden fazla sayfa içerik görüntüleyen bir denetim. |
| TabStrip | `9` | Kullanıcının birden fazla içerik sayfası arasında geçiş yapmasına olanak tanıyan bir denetim. |
| CommandButton | `10` | Tıklandığında bir eylemi tetikleyen bir düğme. |
| Image | `11` | Bir görüntüyü görüntüleyen bir denetim. |
| ScrollBar | `12` | Kullanıcının içerikte gezinmesine olanak tanıyan bir denetim. |
| Form | `13` | Diğer kontroller için bir kapsayıcı. |
| ListBox | `14` | Öğelerin bir listesini görüntüleyen bir denetim. |

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

* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
