---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: .NET için Aspose.Words
description: DocumentBuilder MoveToField yöntemi ile belgelerinizde zahmetsizce gezinin, düzenleme verimliliğini artırmak için imleci herhangi bir alana hızlı bir şekilde taşıyın.
type: docs
weight: 570
url: /tr/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

İmleci belgedeki bir alana taşır.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| field | Field | İmlecin taşınacağı alan. |
| isAfter | Boolean | Ne zaman`doğru` , imleci alan sonundan sonraya taşır. `YANLIŞ`, imleci alan başlangıcından önceye taşır. |

## Örnekler

Bir belge oluşturucunun düğüm ekleme noktası imlecinin belirli bir alana nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// DocumentBuilder'ı kullanarak bir alan ekleyin ve ardından bir metin parçası ekleyin.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Oluşturucunun imleci şu anda belgenin sonunda.
Assert.Null(builder.CurrentNode);

// İmleci alana taşıyın ve imlecin alanın önüne mi yoksa arkasına mı yerleştirileceğini belirtin.
builder.MoveToField(field, moveCursorToAfterTheField);

// Her iki durumda da imlecin alanın dışında olduğuna dikkat edin.
// Bu, alanı oluşturucuyu kullanarak bu şekilde düzenleyemeyeceğimiz anlamına gelir.
// Bir alanı düzenlemek için, alanın FieldStart'ında oluşturucunun MoveTo metodunu kullanabiliriz
// veya imlecin içine yerleştirileceği FieldSeparator düğümü.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
