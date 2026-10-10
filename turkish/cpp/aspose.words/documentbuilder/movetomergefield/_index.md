---
title: "Aspose::Words::DocumentBuilder::MoveToMergeField method"
linktitle: "MoveToMergeField"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToMergeField yöntemi. İmleci belirtilen birleştirme alanının hemen sonrasına taşır ve C++'da birleştirme alanını kaldırır."
type: docs
weight: 58000
url: /tr/cpp/aspose.words/documentbuilder/movetomergefield/
---
## DocumentBuilder::MoveToMergeField(const System::String\&) method


İmleci belirtilen birleştirme alanının hemen sonrasına taşır ve birleştirme alanını kaldırır.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldName | const System::String\& | Posta birleştirme alanının büyük/küçük harfe duyarsız adı. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.
## Açıklamalar


İmleci taşıdıktan sonra bu yöntemin birleştirme alanını belgelerden sildiğini unutmayın.

## Örnekler



Bir belge oluşturucu kullanarak, bir posta birleştirme yerine MERGEFIELD'leri veriyle doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Posta birleştirme sırasında veri kaynağındaki aynı ada sahip sütunlardan veri kabul eden bazı MERGEFIELD'leri ekleyin,
// ve ardından onları manuel olarak doldurun.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToMergeField(const System::String\&, bool, bool) method


Birleştirme alanını belirtilen birleştirme alanına taşır.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToMergeField(const System::String &fieldName, bool isAfter, bool isDeleteField)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldName | const System::String\& | Posta birleştirme alanının büyük/küçük harfe duyarsız adı. |
| isAfter | bool | **true** olduğunda, imleci alanın sonundan sonra konumlandırır. **false** olduğunda, imleci alanın başlangıcından önce konumlandırır. |
| isDeleteField | bool | **true** olduğunda birleştirme alanını siler. |

### ReturnValue

**true** if the merge field was found and the cursor was moved; **false** otherwise.

## Örnekler



Alanların nasıl ekleneceğini ve belge oluşturucunun imlecinin onlara nasıl taşınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
builder->InsertField(u"MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

// İmleci ilk MERGEFIELD'e taşıyın.
builder->MoveToMergeField(u"MyMergeField1", true, false);

// İmlecin ilk MERGEFIELD'den hemen sonra ve ikincisinden önce konumlandırıldığını unutmayın.
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Start(), builder->get_CurrentNode());
ASPOSE_ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_End(), builder->get_CurrentNode()->get_PreviousSibling());

// Oluşturucu kullanarak alanın alan kodunu veya içeriğini düzenlemek istiyorsak,
// imlecinin bir alanın içinde olması gerekir.
// Bunu bir alanın içine yerleştirmek için belge oluşturucunun MoveTo metodunu çağırmamız gerekir
// ve alanın başlangıç ya da ayırıcı düğümünü argüman olarak geçirin.
builder->Write(u" Text between our merge fields. ");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MergeFields.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
