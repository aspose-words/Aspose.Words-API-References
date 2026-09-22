---
title: "Aspose::Words::DocumentBuilder::MoveToField yöntemi"
linktitle: "MoveToField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToField yöntemi. İmleci belgede bir alana C++'ta taşır."
type: docs
weight: 56000
url: /tr/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


İmleci belgede bir alana taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| field | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | İmleci taşımak için alan. |
| isAfter | bool | **true** olduğunda, imleci alanın sonundan sonra konumlandırır. **false** olduğunda, imleci alanın başlangıcından önce konumlandırır. |

## Örnekler



Belge oluşturucusunun düğüm ekleme noktası imlecini belirli bir alana nasıl taşıyacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// DocumentBuilder kullanarak bir alan ekleyin ve sonrasına bir metin koşusu ekleyin.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// Oluşturucunun imleci şu anda belgenin sonunda.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// İmleci alana taşırken, bu imlecin alanın önüne mi yoksa sonrasına mı yerleştirileceğini belirtin.
builder->MoveToField(field, moveCursorToAfterTheField);

// Her iki durumda da imlecin alanın dışında olduğunu unutmayın.
// Bu, alanı oluşturucu kullanarak bu şekilde düzenleyemeyeceğimiz anlamına gelir.
// Bir alanı düzenlemek için, oluşturucunun MoveTo yöntemini bir alanın FieldStart'ı üzerinde kullanabiliriz.
// veya imleci içine yerleştirmek için FieldSeparator düğümü.
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
